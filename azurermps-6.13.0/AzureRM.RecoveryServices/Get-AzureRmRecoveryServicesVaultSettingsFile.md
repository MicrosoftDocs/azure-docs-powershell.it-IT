---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: a0572e73d270a37b3c705018a38b4a88fe88d1e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520879"
---
# <span data-ttu-id="8095c-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8095c-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="8095c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8095c-102">SYNOPSIS</span></span>
<span data-ttu-id="8095c-103">Ottiene il file di impostazioni del Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="8095c-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8095c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8095c-104">SYNTAX</span></span>

### <span data-ttu-id="8095c-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="8095c-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8095c-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="8095c-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8095c-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="8095c-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8095c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8095c-108">DESCRIPTION</span></span>
<span data-ttu-id="8095c-109">Il cmdlet **Get-AzureRmRecoveryServicesVaultSettingsFile** ottiene il file di impostazioni per un Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="8095c-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8095c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8095c-110">EXAMPLES</span></span>

### <span data-ttu-id="8095c-111">Esempio 1: registrare un computer Windows Server o DPM per Azure Backup</span><span class="sxs-lookup"><span data-stu-id="8095c-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="8095c-112">Il primo comando ottiene il Vault denominato TestVault e lo archivia nella variabile $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="8095c-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="8095c-113">Il secondo comando imposta la variabile $CredsPath su C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="8095c-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="8095c-114">L'ultimo comando ottiene il file delle credenziali del Vault per $Vault 01 usando le credenziali in $CredsPath per il backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="8095c-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="8095c-115">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="8095c-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="8095c-116">Il comando ottiene il file delle credenziali del Vault per $Vault 01 di tipo Vault siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="8095c-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="8095c-117">Esempio 3: registrare un computer Windows Server o DPM per Azure Backup</span><span class="sxs-lookup"><span data-stu-id="8095c-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="8095c-118">Il comando ottiene il file delle credenziali del Vault per $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="8095c-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="8095c-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8095c-119">PARAMETERS</span></span>

### <span data-ttu-id="8095c-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="8095c-120">-Backup</span></span>
<span data-ttu-id="8095c-121">Indica che il file delle credenziali del Vault è applicabile a Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="8095c-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8095c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8095c-122">-DefaultProfile</span></span>
<span data-ttu-id="8095c-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8095c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8095c-124">-Path</span><span class="sxs-lookup"><span data-stu-id="8095c-124">-Path</span></span>
<span data-ttu-id="8095c-125">Specifica il percorso del file di impostazioni del Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="8095c-125">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="8095c-126">È possibile scaricare il file dal portale del Vault di ripristino di Azure sito e archiviarlo localmente.</span><span class="sxs-lookup"><span data-stu-id="8095c-126">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="8095c-127">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8095c-127">-SiteFriendlyName</span></span>
<span data-ttu-id="8095c-128">Specifica il nome descrittivo del sito.</span><span class="sxs-lookup"><span data-stu-id="8095c-128">Specifies the site friendly name.</span></span>
<span data-ttu-id="8095c-129">Usare questo parametro se si scaricano le credenziali del Vault per un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="8095c-129">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8095c-130">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="8095c-130">-SiteIdentifier</span></span>
<span data-ttu-id="8095c-131">Specifica l'identificatore del sito.</span><span class="sxs-lookup"><span data-stu-id="8095c-131">Specifies the site identifier.</span></span>
<span data-ttu-id="8095c-132">Usare questo parametro se si scaricano le credenziali del Vault per un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="8095c-132">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8095c-133">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8095c-133">-SiteRecovery</span></span>
<span data-ttu-id="8095c-134">Indica che il file delle credenziali del Vault è applicabile al ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="8095c-134">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8095c-135">-Vault</span><span class="sxs-lookup"><span data-stu-id="8095c-135">-Vault</span></span>
<span data-ttu-id="8095c-136">Specifica l'oggetto del Vault di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="8095c-136">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="8095c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8095c-137">CommonParameters</span></span>
<span data-ttu-id="8095c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8095c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8095c-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8095c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8095c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8095c-140">INPUTS</span></span>

### <span data-ttu-id="8095c-141">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="8095c-141">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="8095c-142">Parameters: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8095c-142">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="8095c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8095c-143">OUTPUTS</span></span>

### <span data-ttu-id="8095c-144">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="8095c-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="8095c-145">Note</span><span class="sxs-lookup"><span data-stu-id="8095c-145">NOTES</span></span>

## <span data-ttu-id="8095c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8095c-146">RELATED LINKS</span></span>

[<span data-ttu-id="8095c-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8095c-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="8095c-148">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8095c-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="8095c-149">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8095c-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


