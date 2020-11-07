---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: d4eb596ed7c6a002239b6e30869830596beba230
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863370"
---
# <span data-ttu-id="06111-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="06111-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="06111-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06111-102">SYNOPSIS</span></span>
<span data-ttu-id="06111-103">Abilita la crittografia in una macchina virtuale in esecuzione di IaaS in Azure.</span><span class="sxs-lookup"><span data-stu-id="06111-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="06111-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06111-104">SYNTAX</span></span>

### <span data-ttu-id="06111-105">AADClientSecretParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06111-105">AADClientSecretParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06111-106">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="06111-106">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06111-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06111-107">DESCRIPTION</span></span>
<span data-ttu-id="06111-108">Il cmdlet **set-AzVMDiskEncryptionExtension** Abilita la crittografia in un'infrastruttura in esecuzione come macchina virtuale Service (IaaS) in Azure.</span><span class="sxs-lookup"><span data-stu-id="06111-108">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="06111-109">Questo cmdlet consente la crittografia installando l'estensione di crittografia disco nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06111-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="06111-110">Se non viene specificato alcun parametro *Name* , viene installata un'estensione con il nome predefinito AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o le macchine virtuali AzureDiskEncryptionForLinux per Linux.</span><span class="sxs-lookup"><span data-stu-id="06111-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="06111-111">Questo cmdlet richiede la conferma da parte degli utenti come uno dei passaggi per abilitare la crittografia richiede il riavvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06111-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="06111-112">È consigliabile salvare il lavoro nella macchina virtuale prima di eseguire questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06111-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="06111-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06111-113">EXAMPLES</span></span>

### <span data-ttu-id="06111-114">Esempio 1: abilitare la crittografia usando l'ID client e il segreto client di Azure AD</span><span class="sxs-lookup"><span data-stu-id="06111-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="06111-115">Questo esempio consente la crittografia usando l'ID client Azure AD e il segreto client.</span><span class="sxs-lookup"><span data-stu-id="06111-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="06111-116">Esempio 2: abilitare la crittografia usando l'identificazione client di Azure AD e la certificazione client</span><span class="sxs-lookup"><span data-stu-id="06111-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
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
Set-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="06111-117">Questo esempio consente la crittografia usando le identificazioni personali Azure AD ID client e certificazione client.</span><span class="sxs-lookup"><span data-stu-id="06111-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="06111-118">Esempio 3: abilitare la crittografia usando l'ID client di Azure AD, il segreto client e la chiave di crittografia del disco a capo usando la chiave di crittografia</span><span class="sxs-lookup"><span data-stu-id="06111-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="06111-119">Questo esempio consente la crittografia usando la chiave di crittografia del disco di Azure AD, il segreto client e la chiave di crittografia dei dischi a capo.</span><span class="sxs-lookup"><span data-stu-id="06111-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="06111-120">Esempio 4: abilitare la crittografia usando l'ID client di Azure AD, l'identificazione digitale client CERT e il wrapping del disco EncryptionKey usando la chiave di crittografia chiave</span><span class="sxs-lookup"><span data-stu-id="06111-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
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
Set-AzureKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="06111-121">Questo esempio consente la crittografia usando l'ID client Azure AD, l'identificazione digitale client CERT e la chiave di crittografia del disco a capo usando la chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="06111-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="06111-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06111-122">PARAMETERS</span></span>

### <span data-ttu-id="06111-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="06111-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="06111-124">Specifica l'identificazione personale del certificato client dell'applicazione della directory AzureActive (Azure AD) che dispone delle autorizzazioni per la scrittura di segreti in un **Vault**.</span><span class="sxs-lookup"><span data-stu-id="06111-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="06111-125">Come prerequisito, il certificato client di Azure AD deve essere distribuito in precedenza nell'archivio certificati del computer locale della macchina virtuale `my` .</span><span class="sxs-lookup"><span data-stu-id="06111-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="06111-126">Il cmdlet Add-AzVMSecret può essere usato per distribuire un certificato in una macchina virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="06111-126">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="06111-127">Per altre informazioni, vedi la guida del cmdlet **Add-AzVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="06111-127">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="06111-128">Il certificato deve essere distribuito in precedenza nel computer locale della macchina virtuale l'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="06111-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: String
Parameter Sets: AADClientCertParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="06111-129">-AadClientID</span></span>
<span data-ttu-id="06111-130">Specifica l'ID client dell'applicazione Azure AD che dispone delle autorizzazioni per la scrittura di segreti in **Vault**.</span><span class="sxs-lookup"><span data-stu-id="06111-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="06111-131">-AadClientSecret</span></span>
<span data-ttu-id="06111-132">Specifica il segreto client dell'applicazione Azure AD che dispone delle autorizzazioni per la scrittura di segreti in **Vault**.</span><span class="sxs-lookup"><span data-stu-id="06111-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: AADClientSecretParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06111-133">-DefaultProfile</span></span>
<span data-ttu-id="06111-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06111-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06111-135">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="06111-135">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="06111-136">Indica che questo cmdlet disabilita l'aggiornamento automatico della versione secondaria dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="06111-136">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-137">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="06111-137">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="06111-138">Specifica l'ID risorsa del **Vault** a cui devono essere caricate le chiavi di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06111-138">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-139">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="06111-139">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="06111-140">Specifica l'URL del **Vault** in cui devono essere caricati le chiavi di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06111-140">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-141">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="06111-141">-EncryptFormatAll</span></span>
<span data-ttu-id="06111-142">Encrypt-Format tutte le unità dati che non sono già crittografate</span><span class="sxs-lookup"><span data-stu-id="06111-142">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06111-143">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="06111-143">-ExtensionPublisherName</span></span>
<span data-ttu-id="06111-144">Nome dell'editore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="06111-144">The extension publisher name.</span></span> <span data-ttu-id="06111-145">Specifica questo parametro solo per eseguire l'override del valore predefinito "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="06111-145">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-146">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="06111-146">-ExtensionType</span></span>
<span data-ttu-id="06111-147">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="06111-147">The extension type.</span></span> <span data-ttu-id="06111-148">Specifica questo parametro per eseguire l'override del valore predefinito "AzureDiskEncryption" per le VM di Windows e "AzureDiskEncryptionForLinux" per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="06111-148">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-149">-Force</span><span class="sxs-lookup"><span data-stu-id="06111-149">-Force</span></span>
<span data-ttu-id="06111-150">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="06111-150">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06111-151">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="06111-151">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="06111-152">Specifica l'algoritmo usato per racchiudere e scartare la chiave di crittografia chiave della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06111-152">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="06111-153">Il valore predefinito è RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="06111-153">The default value is RSA-OAEP.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-154">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="06111-154">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="06111-155">Specifica l'URL della chiave di crittografia chiave usata per eseguire il wrapping e la decodificazione della chiave di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06111-155">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="06111-156">Questo deve essere l'URL con versione completa.</span><span class="sxs-lookup"><span data-stu-id="06111-156">This must be the full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-157">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="06111-157">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="06111-158">Specifica l'ID risorsa del **Vault** che contiene la chiave di crittografia chiave utilizzata per eseguire il wrapping e la decodificazione della chiave di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06111-158">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="06111-159">Questo deve essere un URL con versione completa.</span><span class="sxs-lookup"><span data-stu-id="06111-159">This must be a full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="06111-160">-Name</span></span>
<span data-ttu-id="06111-161">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="06111-161">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="06111-162">Il valore predefinito è AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o le macchine virtuali AzureDiskEncryptionForLinux per Linux.</span><span class="sxs-lookup"><span data-stu-id="06111-162">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-163">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="06111-163">-Passphrase</span></span>
<span data-ttu-id="06111-164">Specifica la passphrase usata solo per crittografare solo le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="06111-164">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="06111-165">Questo parametro non viene usato per le macchine virtuali che eseguono il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="06111-165">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06111-166">-ResourceGroupName</span></span>
<span data-ttu-id="06111-167">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06111-167">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-168">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="06111-168">-SequenceVersion</span></span>
<span data-ttu-id="06111-169">Specifica il numero di sequenza delle operazioni di crittografia per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06111-169">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="06111-170">Questo è univoco per ogni operazione di crittografia eseguita nella stessa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06111-170">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="06111-171">Il cmdlet Get-AzVMExtension può essere usato per recuperare il numero di sequenza precedente usato.</span><span class="sxs-lookup"><span data-stu-id="06111-171">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-172">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="06111-172">-SkipVmBackup</span></span>
<span data-ttu-id="06111-173">Ignorare la creazione di backup per VM Linux</span><span class="sxs-lookup"><span data-stu-id="06111-173">Skip backup creation for Linux VMs</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-174">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="06111-174">-TypeHandlerVersion</span></span>
<span data-ttu-id="06111-175">Specifica la versione dell'estensione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="06111-175">Specifies the version of the encryption extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-176">-VMName</span><span class="sxs-lookup"><span data-stu-id="06111-176">-VMName</span></span>
<span data-ttu-id="06111-177">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06111-177">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-178">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="06111-178">-VolumeType</span></span>
<span data-ttu-id="06111-179">Specifica il tipo di volumi della macchina virtuale per eseguire l'operazione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="06111-179">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="06111-180">I valori consentiti per le macchine virtuali che eseguono il sistema operativo Windows sono i seguenti: All, OS e data.</span><span class="sxs-lookup"><span data-stu-id="06111-180">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="06111-181">I valori consentiti per le macchine virtuali Linux sono i seguenti: solo dati.</span><span class="sxs-lookup"><span data-stu-id="06111-181">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06111-182">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06111-182">-Confirm</span></span>
<span data-ttu-id="06111-183">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06111-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06111-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06111-184">-WhatIf</span></span>
<span data-ttu-id="06111-185">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06111-185">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="06111-186">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06111-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06111-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06111-187">CommonParameters</span></span>
<span data-ttu-id="06111-188">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06111-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06111-189">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06111-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06111-190">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06111-190">INPUTS</span></span>

### <span data-ttu-id="06111-191">Nessuno</span><span class="sxs-lookup"><span data-stu-id="06111-191">None</span></span>
<span data-ttu-id="06111-192">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="06111-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06111-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06111-193">OUTPUTS</span></span>

### <span data-ttu-id="06111-194">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="06111-194">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="06111-195">Note</span><span class="sxs-lookup"><span data-stu-id="06111-195">NOTES</span></span>

## <span data-ttu-id="06111-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06111-196">RELATED LINKS</span></span>

[<span data-ttu-id="06111-197">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="06111-197">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="06111-198">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="06111-198">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="06111-199">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="06111-199">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


