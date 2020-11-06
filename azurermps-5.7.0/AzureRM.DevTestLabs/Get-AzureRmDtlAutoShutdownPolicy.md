---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 557cfcaefef1a85fe7ad0a8bd62f4ddbf0ecb6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512619"
---
# <span data-ttu-id="a801f-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="a801f-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="a801f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a801f-102">SYNOPSIS</span></span>
<span data-ttu-id="a801f-103">Ottiene i criteri di arresto automatico di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="a801f-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a801f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a801f-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a801f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a801f-105">DESCRIPTION</span></span>
<span data-ttu-id="a801f-106">Il cmdlet **Get-AzureRmDtlAutoShutdownPolicy** ottiene i criteri di arresto automatico di un Lab, che consente di arrestare automaticamente tutte le macchine virtuali in un Lab in un determinato momento della giornata.</span><span class="sxs-lookup"><span data-stu-id="a801f-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="a801f-107">Il cmdlet restituisce se lo stato del criterio è abilitato e l'ora del giorno in cui è stata impostata la chiusura automatica delle macchine virtuali Lab.</span><span class="sxs-lookup"><span data-stu-id="a801f-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="a801f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a801f-108">EXAMPLES</span></span>

## <span data-ttu-id="a801f-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a801f-109">PARAMETERS</span></span>

### <span data-ttu-id="a801f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a801f-110">-DefaultProfile</span></span>
<span data-ttu-id="a801f-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a801f-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a801f-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="a801f-112">-LabName</span></span>
<span data-ttu-id="a801f-113">Specifica il nome del Lab per cui questo cmdlet ottiene i criteri di arresto automatico.</span><span class="sxs-lookup"><span data-stu-id="a801f-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a801f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a801f-114">-ResourceGroupName</span></span>
<span data-ttu-id="a801f-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="a801f-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a801f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a801f-116">CommonParameters</span></span>
<span data-ttu-id="a801f-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a801f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a801f-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a801f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a801f-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a801f-119">INPUTS</span></span>

### <span data-ttu-id="a801f-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a801f-120">None</span></span>
<span data-ttu-id="a801f-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a801f-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a801f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a801f-122">OUTPUTS</span></span>

### <span data-ttu-id="a801f-123">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="a801f-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="a801f-124">Questo cmdlet restituisce la programmazione che specifica quando deve essere arrestata la macchina virtuale del Lab.</span><span class="sxs-lookup"><span data-stu-id="a801f-124">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="a801f-125">Note</span><span class="sxs-lookup"><span data-stu-id="a801f-125">NOTES</span></span>

## <span data-ttu-id="a801f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a801f-126">RELATED LINKS</span></span>

[<span data-ttu-id="a801f-127">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="a801f-127">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


