---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 0d074c18ad9b5f9ea34a465acd4a91a88d4b69ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192919"
---
# <span data-ttu-id="446b8-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="446b8-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="446b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="446b8-102">SYNOPSIS</span></span>
<span data-ttu-id="446b8-103">Recupera il file di impostazioni del vault di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="446b8-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="446b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="446b8-104">SYNTAX</span></span>

### <span data-ttu-id="446b8-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="446b8-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="446b8-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="446b8-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="446b8-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="446b8-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="446b8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="446b8-108">DESCRIPTION</span></span>
<span data-ttu-id="446b8-109">Il cmdlet **Get-AzRecoveryServicesVaultSettingsFile** ottiene il file di impostazioni per un vault di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="446b8-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="446b8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="446b8-110">EXAMPLES</span></span>

### <span data-ttu-id="446b8-111">Esempio 1: Registrare un computer Windows Server o DPM per il backup di Azure</span><span class="sxs-lookup"><span data-stu-id="446b8-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="446b8-112">Il primo comando ottiene il vault denominato TestVault e quindi lo archivia nella variabile $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="446b8-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="446b8-113">Il secondo comando imposta la $CredsPath variabile su C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="446b8-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="446b8-114">L'ultimo comando recupera il file delle credenziali del vault per $Vault 01 usando le credenziali in $CredsPath per Il backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="446b8-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="446b8-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="446b8-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="446b8-116">Il comando recupera il file delle credenziali del vault per $Vault 01 di tipo vault siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="446b8-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="446b8-117">Esempio 3: Registrare un computer Windows Server o DPM per il backup di Azure</span><span class="sxs-lookup"><span data-stu-id="446b8-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="446b8-118">Il comando recupera il file delle credenziali del vault per $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="446b8-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="446b8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="446b8-119">PARAMETERS</span></span>

### <span data-ttu-id="446b8-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="446b8-120">-Backup</span></span>
<span data-ttu-id="446b8-121">Indica che il file delle credenziali del vault è applicabile al backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="446b8-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446b8-122">-Certificato</span><span class="sxs-lookup"><span data-stu-id="446b8-122">-Certificate</span></span>
<span data-ttu-id="446b8-123">{{Fill Certificate Description}}</span><span class="sxs-lookup"><span data-stu-id="446b8-123">{{Fill Certificate Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446b8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="446b8-124">-DefaultProfile</span></span>
<span data-ttu-id="446b8-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="446b8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="446b8-126">-Path</span><span class="sxs-lookup"><span data-stu-id="446b8-126">-Path</span></span>
<span data-ttu-id="446b8-127">Specifica il percorso del file di impostazioni del vault di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="446b8-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="446b8-128">È possibile scaricare questo file dal portale del vault di Azure Site Recovery e archiviarlo in locale.</span><span class="sxs-lookup"><span data-stu-id="446b8-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446b8-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="446b8-129">-SiteFriendlyName</span></span>
<span data-ttu-id="446b8-130">Specifica il nome descrittivo del sito.</span><span class="sxs-lookup"><span data-stu-id="446b8-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="446b8-131">Usare questo parametro se si scaricano le credenziali del vault per un sito di Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="446b8-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446b8-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="446b8-132">-SiteIdentifier</span></span>
<span data-ttu-id="446b8-133">Specifica l'identificatore del sito.</span><span class="sxs-lookup"><span data-stu-id="446b8-133">Specifies the site identifier.</span></span>
<span data-ttu-id="446b8-134">Usare questo parametro se si scaricano le credenziali del vault per un sito di Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="446b8-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446b8-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="446b8-135">-SiteRecovery</span></span>
<span data-ttu-id="446b8-136">Indica che il file delle credenziali del vault è applicabile a Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="446b8-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446b8-137">-Vault</span><span class="sxs-lookup"><span data-stu-id="446b8-137">-Vault</span></span>
<span data-ttu-id="446b8-138">Specifica l'oggetto vault di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="446b8-138">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="446b8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="446b8-139">CommonParameters</span></span>
<span data-ttu-id="446b8-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="446b8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="446b8-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="446b8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="446b8-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="446b8-142">INPUTS</span></span>

### <span data-ttu-id="446b8-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="446b8-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="446b8-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="446b8-144">OUTPUTS</span></span>

### <span data-ttu-id="446b8-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="446b8-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="446b8-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="446b8-146">NOTES</span></span>

## <span data-ttu-id="446b8-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="446b8-147">RELATED LINKS</span></span>

[<span data-ttu-id="446b8-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="446b8-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="446b8-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="446b8-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="446b8-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="446b8-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


