---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 621e5ac05c5f975ff3878781bcb8c5a1b40c04bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687433"
---
# <span data-ttu-id="75939-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="75939-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="75939-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75939-102">SYNOPSIS</span></span>
<span data-ttu-id="75939-103">Ottiene il file di impostazioni del caveau di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="75939-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75939-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75939-104">SYNTAX</span></span>

### <span data-ttu-id="75939-105">ByParam (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75939-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75939-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="75939-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75939-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="75939-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75939-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75939-108">DESCRIPTION</span></span>
<span data-ttu-id="75939-109">Il cmdlet **Get-AzureRmSiteRecoveryVaultSettingsFile** ottiene il file di impostazioni per un Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="75939-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="75939-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75939-110">EXAMPLES</span></span>

## <span data-ttu-id="75939-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75939-111">PARAMETERS</span></span>

### <span data-ttu-id="75939-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75939-112">-DefaultProfile</span></span>
<span data-ttu-id="75939-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75939-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75939-114">-Path</span><span class="sxs-lookup"><span data-stu-id="75939-114">-Path</span></span>
<span data-ttu-id="75939-115">Specifica il percorso del file di impostazioni del caveau di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="75939-115">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="75939-116">Per archiviare il file in locale, scaricarlo dal portale del Vault Recovery del sito una volta completato il comando.</span><span class="sxs-lookup"><span data-stu-id="75939-116">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75939-117">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="75939-117">-SiteFriendlyName</span></span>
<span data-ttu-id="75939-118">Specifica il nome descrittivo del sito per il Vault quando il sito è un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="75939-118">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75939-119">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="75939-119">-SiteIdentifier</span></span>
<span data-ttu-id="75939-120">Specifica l'identificatore del sito per il Vault quando il sito è un sito Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="75939-120">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75939-121">-Vault</span><span class="sxs-lookup"><span data-stu-id="75939-121">-Vault</span></span>
<span data-ttu-id="75939-122">Specifica l'oggetto Vault per il sito.</span><span class="sxs-lookup"><span data-stu-id="75939-122">Specifies the vault object for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75939-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75939-123">CommonParameters</span></span>
<span data-ttu-id="75939-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75939-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75939-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75939-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75939-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75939-126">INPUTS</span></span>

### <span data-ttu-id="75939-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="75939-127">ASRVault</span></span>
<span data-ttu-id="75939-128">Il parametro "Vault" accetta il valore di tipo "ASRVault" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="75939-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="75939-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75939-129">OUTPUTS</span></span>

### <span data-ttu-id="75939-130">Microsoft. Azure. Commands. SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="75939-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="75939-131">Note</span><span class="sxs-lookup"><span data-stu-id="75939-131">NOTES</span></span>

## <span data-ttu-id="75939-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75939-132">RELATED LINKS</span></span>

[<span data-ttu-id="75939-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="75939-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="75939-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="75939-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
