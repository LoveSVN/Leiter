# Uncomment the next line to define a global platform for your project
platform :ios, '11.0'
use_frameworks!
install! 'cocoapods',
  :generate_multiple_pod_projects => true

def analytics_and_reporting_pods
    pod 'Amplitude-iOS', '~> 4.3'
end

target 'Leiter' do
    pod 'SPBaseKit', :git => 'https://github.com/Tuluobo/SPBaseKit.git', :commit => 'be5c72d'
    pod 'SnapKit', '~> 4.2.0'
    pod 'ionicons', '~> 2.1.1'
    pod 'MJRefresh', '~> 3.1.15'
    pod 'VTAcknowledgementsViewController', '~> 1.4.1'
    pod 'WCDB.swift', '~> 1.0.7'
    pod 'ReactiveSwift', '~> 6.0'
    pod 'ReactiveCocoa', '~> 10.0'
    pod 'SVProgressHUD', '~> 2.2.5'
    pod 'SGQRCode', '~> 3.0.1'
    pod 'Reveal-SDK', '~> 24',:configurations => ['Debug']
    analytics_and_reporting_pods
end

target 'NEWidget' do
    pod 'SPBaseKit', :git => 'https://github.com/Tuluobo/SPBaseKit.git', :commit => 'be5c72d'
end

post_install do |installer|
  installer.generated_projects.each do |project|
        project.targets.each do |target|
            target.build_configurations.each do |config|
                config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '11.0'
             end
        end
 end
  
end
