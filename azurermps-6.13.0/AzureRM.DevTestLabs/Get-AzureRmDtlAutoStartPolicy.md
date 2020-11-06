---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: efe948e2676b44a70917efb43e901f8848dec0e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513875"
---
# <span data-ttu-id="b43ad-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="b43ad-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="b43ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b43ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b43ad-103">Ottiene i criteri di avvio automatico di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="b43ad-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b43ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b43ad-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b43ad-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b43ad-105">DESCRIPTION</span></span>
<span data-ttu-id="b43ad-106">Il cmdlet **Get-AzureRmDtlAutoStartPolicy** ottiene i criteri di avvio automatico di un Lab che pianifica le macchine virtuali Lab per l'avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="b43ad-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="b43ad-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e i giorni della settimana e l'ora del giorno impostati per consentire la programmazione delle macchine virtuali Lab per l'avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="b43ad-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="b43ad-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b43ad-108">EXAMPLES</span></span>

## <span data-ttu-id="b43ad-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b43ad-109">PARAMETERS</span></span>

### <span data-ttu-id="b43ad-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43ad-110">-DefaultProfile</span></span>
<span data-ttu-id="b43ad-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b43ad-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b43ad-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="b43ad-112">-LabName</span></span>
<span data-ttu-id="b43ad-113">Specifica il nome del Lab per cui questo cmdlet ottiene i criteri di avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="b43ad-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="b43ad-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b43ad-114">-ResourceGroupName</span></span>
<span data-ttu-id="b43ad-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="b43ad-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b43ad-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43ad-116">CommonParameters</span></span>
<span data-ttu-id="b43ad-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b43ad-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43ad-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b43ad-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43ad-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b43ad-119">INPUTS</span></span>

### <span data-ttu-id="b43ad-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b43ad-120">System.String</span></span>

## <span data-ttu-id="b43ad-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b43ad-121">OUTPUTS</span></span>

### <span data-ttu-id="b43ad-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="b43ad-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="b43ad-123">Note</span><span class="sxs-lookup"><span data-stu-id="b43ad-123">NOTES</span></span>

## <span data-ttu-id="b43ad-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b43ad-124">RELATED LINKS</span></span>

[<span data-ttu-id="b43ad-125">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="b43ad-125">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)


