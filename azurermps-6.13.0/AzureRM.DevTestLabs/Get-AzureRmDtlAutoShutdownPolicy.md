---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 04b226a623a31c73ddd92c858f9ab610a533886f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513879"
---
# <span data-ttu-id="be6d0-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="be6d0-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="be6d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="be6d0-103">Ottiene i criteri di arresto automatico di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="be6d0-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be6d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be6d0-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be6d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be6d0-105">DESCRIPTION</span></span>
<span data-ttu-id="be6d0-106">Il cmdlet **Get-AzureRmDtlAutoShutdownPolicy** ottiene i criteri di arresto automatico di un Lab, che consente di arrestare automaticamente tutte le macchine virtuali in un Lab in un determinato momento della giornata.</span><span class="sxs-lookup"><span data-stu-id="be6d0-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="be6d0-107">Il cmdlet restituisce se lo stato del criterio è abilitato e l'ora del giorno in cui è stata impostata la chiusura automatica delle macchine virtuali Lab.</span><span class="sxs-lookup"><span data-stu-id="be6d0-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="be6d0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be6d0-108">EXAMPLES</span></span>

## <span data-ttu-id="be6d0-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be6d0-109">PARAMETERS</span></span>

### <span data-ttu-id="be6d0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be6d0-110">-DefaultProfile</span></span>
<span data-ttu-id="be6d0-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="be6d0-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be6d0-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="be6d0-112">-LabName</span></span>
<span data-ttu-id="be6d0-113">Specifica il nome del Lab per cui questo cmdlet ottiene i criteri di arresto automatico.</span><span class="sxs-lookup"><span data-stu-id="be6d0-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="be6d0-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be6d0-114">-ResourceGroupName</span></span>
<span data-ttu-id="be6d0-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="be6d0-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="be6d0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be6d0-116">CommonParameters</span></span>
<span data-ttu-id="be6d0-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be6d0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be6d0-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be6d0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be6d0-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be6d0-119">INPUTS</span></span>

### <span data-ttu-id="be6d0-120">System. String</span><span class="sxs-lookup"><span data-stu-id="be6d0-120">System.String</span></span>

## <span data-ttu-id="be6d0-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be6d0-121">OUTPUTS</span></span>

### <span data-ttu-id="be6d0-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="be6d0-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="be6d0-123">Note</span><span class="sxs-lookup"><span data-stu-id="be6d0-123">NOTES</span></span>

## <span data-ttu-id="be6d0-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be6d0-124">RELATED LINKS</span></span>

[<span data-ttu-id="be6d0-125">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="be6d0-125">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


