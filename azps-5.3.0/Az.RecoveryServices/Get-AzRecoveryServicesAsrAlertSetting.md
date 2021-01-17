---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384478"
---
# <span data-ttu-id="a3bd7-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="a3bd7-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="a3bd7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="a3bd7-103">Ottiene le impostazioni di notifica di ripristino del sito Azure configurate per il Vault.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="a3bd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3bd7-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3bd7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3bd7-105">DESCRIPTION</span></span>
<span data-ttu-id="a3bd7-106">Il cmdlet **Get-AzRecoveryServicesAsrAlertSetting** ottiene le impostazioni di notifica di ripristino di Azure site configurate per il Vault.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="a3bd7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3bd7-107">EXAMPLES</span></span>

### <span data-ttu-id="a3bd7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3bd7-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="a3bd7-109">Ottenere l'impostazione avviso/notifica per il ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="a3bd7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3bd7-110">PARAMETERS</span></span>

### <span data-ttu-id="a3bd7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3bd7-111">-DefaultProfile</span></span>
<span data-ttu-id="a3bd7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3bd7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3bd7-113">CommonParameters</span></span>
<span data-ttu-id="a3bd7-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3bd7-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3bd7-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3bd7-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3bd7-116">INPUTS</span></span>

### <span data-ttu-id="a3bd7-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a3bd7-117">None</span></span>

## <span data-ttu-id="a3bd7-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3bd7-118">OUTPUTS</span></span>

### <span data-ttu-id="a3bd7-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="a3bd7-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="a3bd7-120">Note</span><span class="sxs-lookup"><span data-stu-id="a3bd7-120">NOTES</span></span>

## <span data-ttu-id="a3bd7-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3bd7-121">RELATED LINKS</span></span>
