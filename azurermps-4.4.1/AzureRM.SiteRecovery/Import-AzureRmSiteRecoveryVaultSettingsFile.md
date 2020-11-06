---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 42863e0dbf6982ced1f77f916c97ed4fc19d6979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521130"
---
# <span data-ttu-id="38820-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="38820-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="38820-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38820-102">SYNOPSIS</span></span>
<span data-ttu-id="38820-103">Importa un file di impostazioni del caveau di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="38820-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38820-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38820-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38820-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38820-105">DESCRIPTION</span></span>
<span data-ttu-id="38820-106">Il cmdlet **Import-AzureRmSiteRecoveryVaultSettingsFile** importa un file di impostazioni del Vault di ripristino di Azure site per impostare il contesto del Vault per le successive operazioni di ripristino del sito nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="38820-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="38820-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38820-107">EXAMPLES</span></span>

## <span data-ttu-id="38820-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38820-108">PARAMETERS</span></span>

### <span data-ttu-id="38820-109">-Path</span><span class="sxs-lookup"><span data-stu-id="38820-109">-Path</span></span>
<span data-ttu-id="38820-110">Specifica il percorso del file di impostazioni del caveau di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="38820-110">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="38820-111">Questo file può essere scaricato dal portale della volta di ripristino del sito e archiviato localmente.</span><span class="sxs-lookup"><span data-stu-id="38820-111">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

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

### <span data-ttu-id="38820-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38820-112">-DefaultProfile</span></span>
<span data-ttu-id="38820-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38820-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38820-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38820-114">CommonParameters</span></span>
<span data-ttu-id="38820-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38820-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38820-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38820-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38820-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38820-117">INPUTS</span></span>

## <span data-ttu-id="38820-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38820-118">OUTPUTS</span></span>

### <span data-ttu-id="38820-119">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="38820-119">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="38820-120">Note</span><span class="sxs-lookup"><span data-stu-id="38820-120">NOTES</span></span>

## <span data-ttu-id="38820-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38820-121">RELATED LINKS</span></span>

[<span data-ttu-id="38820-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="38820-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
