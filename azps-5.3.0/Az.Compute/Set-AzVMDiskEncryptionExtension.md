---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 1c69d79e148eae92307855ecfe308f5208a2f455
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488159"
---
# <span data-ttu-id="0fffc-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0fffc-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="0fffc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0fffc-102">SYNOPSIS</span></span>
<span data-ttu-id="0fffc-103">Abilita la crittografia in una macchina virtuale in esecuzione di IaaS in Azure.</span><span class="sxs-lookup"><span data-stu-id="0fffc-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="0fffc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fffc-104">SYNTAX</span></span>

### <span data-ttu-id="0fffc-105">SinglePassParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0fffc-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fffc-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fffc-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fffc-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fffc-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fffc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fffc-108">DESCRIPTION</span></span>
<span data-ttu-id="0fffc-109">Il cmdlet **set-AzVMDiskEncryptionExtension** Abilita la crittografia in un'infrastruttura in esecuzione come macchina virtuale Service (IaaS) in Azure.</span><span class="sxs-lookup"><span data-stu-id="0fffc-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="0fffc-110">Consente la crittografia installando l'estensione di crittografia disco nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fffc-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="0fffc-111">Questo cmdlet richiede la conferma da parte degli utenti come uno dei passaggi per abilitare la crittografia richiede il riavvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fffc-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="0fffc-112">È consigliabile salvare il lavoro nella macchina virtuale prima di eseguire questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fffc-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="0fffc-113">Linux: il parametro **VolumeType** è necessario quando si crittografano le macchine virtuali Linux e deve essere impostato su un valore ("OS", "dati" o "tutti") supportato dalla distribuzione Linux.</span><span class="sxs-lookup"><span data-stu-id="0fffc-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="0fffc-114">Windows: il parametro **VolumeType** può essere omesso, in questo caso l'operazione viene impostata su tutte per impostazione predefinita; Se il parametro VolumeType è presente per una macchina virtuale di Windows, è necessario che sia impostato su All o OS.</span><span class="sxs-lookup"><span data-stu-id="0fffc-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="0fffc-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fffc-115">EXAMPLES</span></span>

### <span data-ttu-id="0fffc-116">Esempio 1: abilitare la crittografia</span><span class="sxs-lookup"><span data-stu-id="0fffc-116">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="0fffc-117">Questo esempio consente la crittografia in una VM senza specificare le credenziali degli annunci.</span><span class="sxs-lookup"><span data-stu-id="0fffc-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="0fffc-118">Esempio 2: abilitare la crittografia con l'input da pipeline</span><span class="sxs-lookup"><span data-stu-id="0fffc-118">Example 2: Enable encryption with pipelined input</span></span>
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

$params | Set-AzVmDiskEncryptionExtension
```

<span data-ttu-id="0fffc-119">Questo esempio Invia parametri usando l'input da pipeline per abilitare la crittografia in una VM, senza specificare le credenziali degli annunci.</span><span class="sxs-lookup"><span data-stu-id="0fffc-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="0fffc-120">Esempio 3: abilitare la crittografia usando l'ID client e il segreto client di Azure AD</span><span class="sxs-lookup"><span data-stu-id="0fffc-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="0fffc-121">Questo esempio usa l'ID client di Azure AD e il segreto client per abilitare la crittografia in una VM.</span><span class="sxs-lookup"><span data-stu-id="0fffc-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="0fffc-122">Esempio 4: abilitare la crittografia usando l'identificazione client di Azure AD e la certificazione client</span><span class="sxs-lookup"><span data-stu-id="0fffc-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="0fffc-123">Questo esempio usa le identificazioni personali di Azure AD ID client e certificazione client per abilitare la crittografia in una VM.</span><span class="sxs-lookup"><span data-stu-id="0fffc-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="0fffc-124">Esempio 5: abilitare la crittografia usando l'ID client di Azure AD, il segreto client e la chiave di crittografia del disco a capo usando la chiave di crittografia</span><span class="sxs-lookup"><span data-stu-id="0fffc-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="0fffc-125">Questo esempio usa l'ID client di Azure AD e il segreto client per abilitare la crittografia in una VM e avvolge la chiave di crittografia del disco con una chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0fffc-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="0fffc-126">Esempio 6: abilitare la crittografia usando l'ID client di Azure AD, l'identificazione digitale client CERT e il wrapping del disco EncryptionKey usando la chiave di crittografia chiave</span><span class="sxs-lookup"><span data-stu-id="0fffc-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid
$VolumeType = "All"

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="0fffc-127">Questo esempio usa l'ID client di Azure AD e l'identificazione personale CERT client per abilitare la crittografia in una VM e avvolge la chiave di crittografia del disco con una chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0fffc-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="0fffc-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0fffc-128">PARAMETERS</span></span>

### <span data-ttu-id="0fffc-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="0fffc-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="0fffc-130">Specifica l'identificazione personale del certificato client dell'applicazione della directory AzureActive (Azure AD) che dispone delle autorizzazioni per la scrittura di segreti in un **Vault**.</span><span class="sxs-lookup"><span data-stu-id="0fffc-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="0fffc-131">Come prerequisito, il certificato client di Azure AD deve essere distribuito in precedenza nell'archivio certificati del computer locale della macchina virtuale `my` .</span><span class="sxs-lookup"><span data-stu-id="0fffc-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="0fffc-132">Il cmdlet Add-AzVMSecret può essere usato per distribuire un certificato in una macchina virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="0fffc-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="0fffc-133">Per altre informazioni, vedi la guida del cmdlet **Add-AzVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="0fffc-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="0fffc-134">Il certificato deve essere distribuito in precedenza nel computer locale della macchina virtuale l'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="0fffc-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="0fffc-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="0fffc-135">-AadClientID</span></span>
<span data-ttu-id="0fffc-136">Specifica l'ID client dell'applicazione Azure AD che dispone delle autorizzazioni per la scrittura di segreti in **Vault**.</span><span class="sxs-lookup"><span data-stu-id="0fffc-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="0fffc-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="0fffc-137">-AadClientSecret</span></span>
<span data-ttu-id="0fffc-138">Specifica il segreto client dell'applicazione Azure AD che dispone delle autorizzazioni per la scrittura di segreti in **Vault**.</span><span class="sxs-lookup"><span data-stu-id="0fffc-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="0fffc-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fffc-139">-DefaultProfile</span></span>
<span data-ttu-id="0fffc-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0fffc-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fffc-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0fffc-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0fffc-142">Indica che questo cmdlet disabilita l'aggiornamento automatico della versione secondaria dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="0fffc-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="0fffc-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0fffc-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="0fffc-144">Specifica l'ID risorsa del **Vault** a cui devono essere caricate le chiavi di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fffc-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="0fffc-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="0fffc-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="0fffc-146">Specifica l'URL del **Vault** in cui devono essere caricati le chiavi di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fffc-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="0fffc-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="0fffc-147">-EncryptFormatAll</span></span>
<span data-ttu-id="0fffc-148">Encrypt-Format tutte le unità dati che non sono già crittografate</span><span class="sxs-lookup"><span data-stu-id="0fffc-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="0fffc-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="0fffc-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="0fffc-150">Nome dell'editore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="0fffc-150">The extension publisher name.</span></span> <span data-ttu-id="0fffc-151">Specifica questo parametro solo per eseguire l'override del valore predefinito "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="0fffc-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="0fffc-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="0fffc-152">-ExtensionType</span></span>
<span data-ttu-id="0fffc-153">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="0fffc-153">The extension type.</span></span> <span data-ttu-id="0fffc-154">Specifica questo parametro per eseguire l'override del valore predefinito "AzureDiskEncryption" per le VM di Windows e "AzureDiskEncryptionForLinux" per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="0fffc-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="0fffc-155">-Force</span><span class="sxs-lookup"><span data-stu-id="0fffc-155">-Force</span></span>
<span data-ttu-id="0fffc-156">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0fffc-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0fffc-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0fffc-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="0fffc-158">Specifica l'algoritmo usato per racchiudere e scartare la chiave di crittografia chiave della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fffc-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="0fffc-159">Il valore predefinito è RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="0fffc-159">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="0fffc-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="0fffc-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="0fffc-161">Specifica l'URL della chiave di crittografia chiave usata per eseguire il wrapping e la decodificazione della chiave di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fffc-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="0fffc-162">Questo deve essere l'URL con versione completa.</span><span class="sxs-lookup"><span data-stu-id="0fffc-162">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="0fffc-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0fffc-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="0fffc-164">Specifica l'ID risorsa del **Vault** che contiene la chiave di crittografia chiave utilizzata per eseguire il wrapping e la decodificazione della chiave di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fffc-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="0fffc-165">Questo deve essere un URL con versione completa.</span><span class="sxs-lookup"><span data-stu-id="0fffc-165">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="0fffc-166">-Nome</span><span class="sxs-lookup"><span data-stu-id="0fffc-166">-Name</span></span>
<span data-ttu-id="0fffc-167">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="0fffc-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="0fffc-168">Se il parametro *Name* viene omesso, l'estensione installata sarà denominata AzureDiskEncryption in Windows Virtual Machines e AzureDiskEncryptionForLinux in macchine virtuali di Linux.</span><span class="sxs-lookup"><span data-stu-id="0fffc-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


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

### <span data-ttu-id="0fffc-169">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="0fffc-169">-Passphrase</span></span>
<span data-ttu-id="0fffc-170">Specifica la passphrase usata solo per crittografare solo le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="0fffc-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="0fffc-171">Questo parametro non viene usato per le macchine virtuali che eseguono il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="0fffc-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="0fffc-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fffc-172">-ResourceGroupName</span></span>
<span data-ttu-id="0fffc-173">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fffc-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0fffc-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="0fffc-174">-SequenceVersion</span></span>
<span data-ttu-id="0fffc-175">Specifica il numero di sequenza delle operazioni di crittografia per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fffc-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="0fffc-176">Questo è univoco per ogni operazione di crittografia eseguita nella stessa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fffc-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="0fffc-177">Il cmdlet Get-AzVMExtension può essere usato per recuperare il numero di sequenza precedente usato.</span><span class="sxs-lookup"><span data-stu-id="0fffc-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="0fffc-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="0fffc-178">-SkipVmBackup</span></span>
<span data-ttu-id="0fffc-179">Ignorare la creazione di backup per VM Linux</span><span class="sxs-lookup"><span data-stu-id="0fffc-179">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="0fffc-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0fffc-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="0fffc-181">Specifica la versione dell'estensione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0fffc-181">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="0fffc-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="0fffc-182">-VMName</span></span>
<span data-ttu-id="0fffc-183">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fffc-183">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0fffc-184">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="0fffc-184">-VolumeType</span></span>
<span data-ttu-id="0fffc-185">Specifica il tipo di volumi della macchina virtuale su cui eseguire l'operazione di crittografia: OS, dati o tutti.</span><span class="sxs-lookup"><span data-stu-id="0fffc-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="0fffc-186">Linux: il parametro **VolumeType** è necessario quando si crittografano le macchine virtuali Linux e deve essere impostato su un valore ("OS", "dati" o "tutti") supportato dalla distribuzione Linux.</span><span class="sxs-lookup"><span data-stu-id="0fffc-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="0fffc-187">Windows: il parametro **VolumeType** può essere omesso, in questo caso l'operazione viene impostata su tutte per impostazione predefinita; Se il parametro VolumeType è presente per una macchina virtuale di Windows, è necessario che sia impostato su All o OS.</span><span class="sxs-lookup"><span data-stu-id="0fffc-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

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

### <span data-ttu-id="0fffc-188">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0fffc-188">-Confirm</span></span>
<span data-ttu-id="0fffc-189">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fffc-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fffc-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fffc-190">-WhatIf</span></span>
<span data-ttu-id="0fffc-191">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fffc-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fffc-192">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fffc-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fffc-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fffc-193">CommonParameters</span></span>
<span data-ttu-id="0fffc-194">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fffc-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fffc-195">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fffc-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fffc-196">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0fffc-196">INPUTS</span></span>

### <span data-ttu-id="0fffc-197">System. String</span><span class="sxs-lookup"><span data-stu-id="0fffc-197">System.String</span></span>

### <span data-ttu-id="0fffc-198">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0fffc-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0fffc-199">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fffc-199">OUTPUTS</span></span>

### <span data-ttu-id="0fffc-200">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0fffc-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0fffc-201">Note</span><span class="sxs-lookup"><span data-stu-id="0fffc-201">NOTES</span></span>

## <span data-ttu-id="0fffc-202">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fffc-202">RELATED LINKS</span></span>

[<span data-ttu-id="0fffc-203">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="0fffc-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="0fffc-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="0fffc-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="0fffc-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0fffc-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


