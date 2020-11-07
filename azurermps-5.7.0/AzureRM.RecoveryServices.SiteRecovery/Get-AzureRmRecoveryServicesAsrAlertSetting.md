---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: d1da03455fad47d889269c0d961def70df6837e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686709"
---
# <span data-ttu-id="e31ff-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="e31ff-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="e31ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e31ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e31ff-103">Ottiene le impostazioni di notifica di ripristino del sito Azure configurate per il Vault.</span><span class="sxs-lookup"><span data-stu-id="e31ff-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e31ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e31ff-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e31ff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e31ff-105">DESCRIPTION</span></span>
<span data-ttu-id="e31ff-106">Il cmdlet **Get-AzureRmRecoveryServicesAsrAlertSetting** ottiene le impostazioni di notifica di ripristino di Azure site configurate per il Vault.</span><span class="sxs-lookup"><span data-stu-id="e31ff-106">The **Get-AzureRmRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="e31ff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e31ff-107">EXAMPLES</span></span>

### <span data-ttu-id="e31ff-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e31ff-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="e31ff-109">Ottenere l'impostazione avviso/notifica per il ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="e31ff-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="e31ff-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e31ff-110">PARAMETERS</span></span>

### <span data-ttu-id="e31ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e31ff-111">-DefaultProfile</span></span>
<span data-ttu-id="e31ff-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e31ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e31ff-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e31ff-113">CommonParameters</span></span>
<span data-ttu-id="e31ff-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e31ff-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e31ff-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e31ff-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e31ff-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e31ff-116">INPUTS</span></span>

### <span data-ttu-id="e31ff-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e31ff-117">None</span></span>

## <span data-ttu-id="e31ff-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e31ff-118">OUTPUTS</span></span>

### <span data-ttu-id="e31ff-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e31ff-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e31ff-120">Note</span><span class="sxs-lookup"><span data-stu-id="e31ff-120">NOTES</span></span>

## <span data-ttu-id="e31ff-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e31ff-121">RELATED LINKS</span></span>