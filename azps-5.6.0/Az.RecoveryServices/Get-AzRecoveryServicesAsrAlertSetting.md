---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: cadde5ec773452897aa9c6915a5f3e16f00cfef5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007678"
---
# <span data-ttu-id="88734-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="88734-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="88734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88734-102">SYNOPSIS</span></span>
<span data-ttu-id="88734-103">Recupera le impostazioni di notifica di Azure Site Recovery configurate per il vault.</span><span class="sxs-lookup"><span data-stu-id="88734-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="88734-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88734-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88734-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="88734-105">DESCRIPTION</span></span>
<span data-ttu-id="88734-106">Il cmdlet **Get-AzRecoveryServicesAsrAlertSetting** ottiene le impostazioni di notifica di Azure Site Recovery configurate per il vault.</span><span class="sxs-lookup"><span data-stu-id="88734-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="88734-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88734-107">EXAMPLES</span></span>

### <span data-ttu-id="88734-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88734-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="88734-109">Impostazione di avviso/notifica per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="88734-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="88734-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88734-110">PARAMETERS</span></span>

### <span data-ttu-id="88734-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88734-111">-DefaultProfile</span></span>
<span data-ttu-id="88734-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88734-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88734-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88734-113">CommonParameters</span></span>
<span data-ttu-id="88734-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88734-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88734-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88734-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88734-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="88734-116">INPUTS</span></span>

### <span data-ttu-id="88734-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="88734-117">None</span></span>

## <span data-ttu-id="88734-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88734-118">OUTPUTS</span></span>

### <span data-ttu-id="88734-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="88734-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="88734-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="88734-120">NOTES</span></span>

## <span data-ttu-id="88734-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88734-121">RELATED LINKS</span></span>
