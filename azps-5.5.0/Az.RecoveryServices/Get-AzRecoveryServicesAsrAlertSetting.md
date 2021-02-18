---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202095"
---
# <span data-ttu-id="518f9-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="518f9-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="518f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="518f9-102">SYNOPSIS</span></span>
<span data-ttu-id="518f9-103">Recupera le impostazioni di notifica di Azure Site Recovery configurate per il vault.</span><span class="sxs-lookup"><span data-stu-id="518f9-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="518f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="518f9-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="518f9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="518f9-105">DESCRIPTION</span></span>
<span data-ttu-id="518f9-106">Il cmdlet **Get-AzRecoveryServicesAsrAlertSetting** ottiene le impostazioni di notifica di Azure Site Recovery configurate per il vault.</span><span class="sxs-lookup"><span data-stu-id="518f9-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="518f9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="518f9-107">EXAMPLES</span></span>

### <span data-ttu-id="518f9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="518f9-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="518f9-109">Impostazione di avviso/notifica per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="518f9-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="518f9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="518f9-110">PARAMETERS</span></span>

### <span data-ttu-id="518f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="518f9-111">-DefaultProfile</span></span>
<span data-ttu-id="518f9-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="518f9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="518f9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="518f9-113">CommonParameters</span></span>
<span data-ttu-id="518f9-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="518f9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="518f9-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="518f9-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="518f9-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="518f9-116">INPUTS</span></span>

### <span data-ttu-id="518f9-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="518f9-117">None</span></span>

## <span data-ttu-id="518f9-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="518f9-118">OUTPUTS</span></span>

### <span data-ttu-id="518f9-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="518f9-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="518f9-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="518f9-120">NOTES</span></span>

## <span data-ttu-id="518f9-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="518f9-121">RELATED LINKS</span></span>
