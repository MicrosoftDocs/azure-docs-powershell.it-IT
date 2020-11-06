---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 3eb2c1c175f52f980ecd451bb7a9474984543f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515464"
---
# <span data-ttu-id="a2a8d-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a2a8d-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="a2a8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a8d-103">Abilita la crittografia in una macchina virtuale in esecuzione di IaaS in Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2a8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2a8d-104">SYNTAX</span></span>

### <span data-ttu-id="a2a8d-105">SinglePassParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2a8d-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2a8d-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2a8d-106">AADClientSecretParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2a8d-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2a8d-107">AADClientCertParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2a8d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2a8d-108">DESCRIPTION</span></span>
<span data-ttu-id="a2a8d-109">Il cmdlet **set-AzureRmVMDiskEncryptionExtension** Abilita la crittografia in un'infrastruttura in esecuzione come macchina virtuale Service (IaaS) in Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-109">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="a2a8d-110">Questo cmdlet consente la crittografia installando l'estensione di crittografia disco nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-110">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="a2a8d-111">Se non viene specificato alcun parametro *Name* , viene installata un'estensione con il nome predefinito AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o le macchine virtuali AzureDiskEncryptionForLinux per Linux.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-111">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="a2a8d-112">Questo cmdlet richiede la conferma da parte degli utenti come uno dei passaggi per abilitare la crittografia richiede il riavvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-112">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="a2a8d-113">È consigliabile salvare il lavoro nella macchina virtuale prima di eseguire questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-113">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="a2a8d-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2a8d-114">EXAMPLES</span></span>

### <span data-ttu-id="a2a8d-115">Esempio 1: abilitare la crittografia</span><span class="sxs-lookup"><span data-stu-id="a2a8d-115">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="a2a8d-116">Questo esempio illustra come abilitare la crittografia senza specificare le credenziali degli annunci.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-116">This example demonstrates enabling encryption without specifying AD credentials.</span></span>

### <span data-ttu-id="a2a8d-117">Esempio 2: abilitare la crittografia con l'input da pipeline</span><span class="sxs-lookup"><span data-stu-id="a2a8d-117">Example 2: Enable encryption with pipelined input</span></span>
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzureRmVmDiskEncryptionExtension
```

<span data-ttu-id="a2a8d-118">Questo esempio illustra l'invio di parametri usando l'input da pipeline per abilitare la crittografia senza specificare le credenziali degli annunci.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-118">This example demonstrates sending parameters using pipelined input to enable encryption without specifying AD credentials.</span></span>

### <span data-ttu-id="a2a8d-119">Esempio 3: abilitare la crittografia usando l'ID client e il segreto client di Azure AD</span><span class="sxs-lookup"><span data-stu-id="a2a8d-119">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="a2a8d-120">Questo esempio consente la crittografia usando l'ID client Azure AD e il segreto client.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-120">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="a2a8d-121">Esempio 4: abilitare la crittografia usando l'identificazione client di Azure AD e la certificazione client</span><span class="sxs-lookup"><span data-stu-id="a2a8d-121">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    {
        "data" : "$filecontentencoded",
        "dataType" : "pfx",
        "password" : "$CertPassword"
    }
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="a2a8d-122">Questo esempio consente la crittografia usando le identificazioni personali Azure AD ID client e certificazione client.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-122">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="a2a8d-123">Esempio 5: abilitare la crittografia usando l'ID client di Azure AD, il segreto client e la chiave di crittografia del disco a capo usando la chiave di crittografia</span><span class="sxs-lookup"><span data-stu-id="a2a8d-123">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="a2a8d-124">Questo esempio consente la crittografia usando la chiave di crittografia del disco di Azure AD, il segreto client e la chiave di crittografia dei dischi a capo.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-124">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="a2a8d-125">Esempio 6: abilitare la crittografia usando l'ID client di Azure AD, l'identificazione digitale client CERT e il wrapping del disco EncryptionKey usando la chiave di crittografia chiave</span><span class="sxs-lookup"><span data-stu-id="a2a8d-125">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    {
        "data" : "$filecontentencoded",
        "dataType" : "pfx",
        "password" : "$CertPassword"
    }
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzureKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="a2a8d-126">Questo esempio consente la crittografia usando l'ID client Azure AD, l'identificazione digitale client CERT e la chiave di crittografia del disco a capo usando la chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-126">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="a2a8d-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2a8d-127">PARAMETERS</span></span>

### <span data-ttu-id="a2a8d-128">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="a2a8d-128">-AadClientCertThumbprint</span></span>
<span data-ttu-id="a2a8d-129">Specifica l'identificazione personale del certificato client dell'applicazione della directory AzureActive (Azure AD) che dispone delle autorizzazioni per la scrittura di segreti in un **Vault**.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-129">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="a2a8d-130">Come prerequisito, il certificato client di Azure AD deve essere distribuito in precedenza nell'archivio certificati del computer locale della macchina virtuale `my` .</span><span class="sxs-lookup"><span data-stu-id="a2a8d-130">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="a2a8d-131">Il cmdlet Add-AzureRmVMSecret può essere usato per distribuire un certificato in una macchina virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-131">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="a2a8d-132">Per altre informazioni, vedi la guida del cmdlet **Add-AzureRmVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="a2a8d-132">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="a2a8d-133">Il certificato deve essere distribuito in precedenza nel computer locale della macchina virtuale l'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-133">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-134">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="a2a8d-134">-AadClientID</span></span>
<span data-ttu-id="a2a8d-135">Specifica l'ID client dell'applicazione Azure AD che dispone delle autorizzazioni per la scrittura di segreti in **Vault**.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-135">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-136">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="a2a8d-136">-AadClientSecret</span></span>
<span data-ttu-id="a2a8d-137">Specifica il segreto client dell'applicazione Azure AD che dispone delle autorizzazioni per la scrittura di segreti in **Vault**.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-137">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a8d-138">-DefaultProfile</span></span>
<span data-ttu-id="a2a8d-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-140">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a2a8d-140">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a2a8d-141">Indica che questo cmdlet disabilita l'aggiornamento automatico della versione secondaria dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-141">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-142">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="a2a8d-142">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="a2a8d-143">Specifica l'ID risorsa del **Vault** a cui devono essere caricate le chiavi di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-143">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-144">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="a2a8d-144">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="a2a8d-145">Specifica l'URL del **Vault** in cui devono essere caricati le chiavi di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-145">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-146">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="a2a8d-146">-EncryptFormatAll</span></span>
<span data-ttu-id="a2a8d-147">Encrypt-Format tutte le unità dati che non sono già crittografate</span><span class="sxs-lookup"><span data-stu-id="a2a8d-147">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-148">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="a2a8d-148">-ExtensionPublisherName</span></span>
<span data-ttu-id="a2a8d-149">Nome dell'editore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-149">The extension publisher name.</span></span> <span data-ttu-id="a2a8d-150">Specifica questo parametro solo per eseguire l'override del valore predefinito "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="a2a8d-150">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-151">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="a2a8d-151">-ExtensionType</span></span>
<span data-ttu-id="a2a8d-152">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-152">The extension type.</span></span> <span data-ttu-id="a2a8d-153">Specifica questo parametro per eseguire l'override del valore predefinito "AzureDiskEncryption" per le VM di Windows e "AzureDiskEncryptionForLinux" per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-153">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-154">-Force</span><span class="sxs-lookup"><span data-stu-id="a2a8d-154">-Force</span></span>
<span data-ttu-id="a2a8d-155">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-155">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-156">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="a2a8d-156">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="a2a8d-157">Specifica l'algoritmo usato per racchiudere e scartare la chiave di crittografia chiave della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-157">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="a2a8d-158">Il valore predefinito è RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-158">The default value is RSA-OAEP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-159">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="a2a8d-159">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="a2a8d-160">Specifica l'URL della chiave di crittografia chiave usata per eseguire il wrapping e la decodificazione della chiave di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-160">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="a2a8d-161">Questo deve essere l'URL con versione completa.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-161">This must be the full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-162">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="a2a8d-162">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="a2a8d-163">Specifica l'ID risorsa del **Vault** che contiene la chiave di crittografia chiave utilizzata per eseguire il wrapping e la decodificazione della chiave di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-163">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="a2a8d-164">Questo deve essere un URL con versione completa.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-164">This must be a full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-165">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2a8d-165">-Name</span></span>
<span data-ttu-id="a2a8d-166">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-166">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="a2a8d-167">Il valore predefinito è AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o le macchine virtuali AzureDiskEncryptionForLinux per Linux.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-167">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-168">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="a2a8d-168">-Passphrase</span></span>
<span data-ttu-id="a2a8d-169">Specifica la passphrase usata solo per crittografare solo le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-169">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="a2a8d-170">Questo parametro non viene usato per le macchine virtuali che eseguono il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-170">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2a8d-171">-ResourceGroupName</span></span>
<span data-ttu-id="a2a8d-172">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-172">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-173">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="a2a8d-173">-SequenceVersion</span></span>
<span data-ttu-id="a2a8d-174">Specifica il numero di sequenza delle operazioni di crittografia per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-174">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="a2a8d-175">Questo è univoco per ogni operazione di crittografia eseguita nella stessa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-175">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="a2a8d-176">Il cmdlet Get-AzureRmVMExtension può essere usato per recuperare il numero di sequenza precedente usato.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-176">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-177">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="a2a8d-177">-SkipVmBackup</span></span>
<span data-ttu-id="a2a8d-178">Ignorare la creazione di backup per VM Linux</span><span class="sxs-lookup"><span data-stu-id="a2a8d-178">Skip backup creation for Linux VMs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-179">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a2a8d-179">-TypeHandlerVersion</span></span>
<span data-ttu-id="a2a8d-180">Specifica la versione dell'estensione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-180">Specifies the version of the encryption extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-181">-VMName</span><span class="sxs-lookup"><span data-stu-id="a2a8d-181">-VMName</span></span>
<span data-ttu-id="a2a8d-182">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-183">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="a2a8d-183">-VolumeType</span></span>
<span data-ttu-id="a2a8d-184">Specifica il tipo di volumi della macchina virtuale per eseguire l'operazione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-184">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="a2a8d-185">I valori consentiti per le macchine virtuali che eseguono il sistema operativo Windows sono i seguenti: All, OS e data.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-185">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="a2a8d-186">I valori consentiti per le macchine virtuali Linux sono i seguenti: All, OS e dati quando supportati dalla distribuzione Linux.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-186">The allowed values for Linux virtual machines are as follows: All, OS, and Data when supported by the Linux distribution.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-187">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a2a8d-187">-Confirm</span></span>
<span data-ttu-id="a2a8d-188">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2a8d-189">-WhatIf</span></span>
<span data-ttu-id="a2a8d-190">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2a8d-191">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a8d-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a8d-192">CommonParameters</span></span>
<span data-ttu-id="a2a8d-193">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2a8d-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a8d-194">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2a8d-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a8d-195">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2a8d-195">INPUTS</span></span>

### <span data-ttu-id="a2a8d-196">System. String</span><span class="sxs-lookup"><span data-stu-id="a2a8d-196">System.String</span></span>

### <span data-ttu-id="a2a8d-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a2a8d-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a2a8d-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2a8d-198">OUTPUTS</span></span>

### <span data-ttu-id="a2a8d-199">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a2a8d-199">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a2a8d-200">Note</span><span class="sxs-lookup"><span data-stu-id="a2a8d-200">NOTES</span></span>

## <span data-ttu-id="a2a8d-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2a8d-201">RELATED LINKS</span></span>

[<span data-ttu-id="a2a8d-202">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="a2a8d-202">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="a2a8d-203">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="a2a8d-203">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="a2a8d-204">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a2a8d-204">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

