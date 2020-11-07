---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b34a60fa2b85f18a5bee10e0e1f66a4ab102c7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674575"
---
# <span data-ttu-id="ad3ae-101">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="ad3ae-101">Get-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="ad3ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad3ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3ae-103">Ottiene i criteri di arresto automatico di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="ad3ae-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="ad3ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad3ae-104">SYNTAX</span></span>

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad3ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad3ae-105">DESCRIPTION</span></span>
<span data-ttu-id="ad3ae-106">Il cmdlet **Get-AzDtlAutoShutdownPolicy** ottiene i criteri di arresto automatico di un Lab, che consente di arrestare automaticamente tutte le macchine virtuali in un Lab in un determinato momento della giornata.</span><span class="sxs-lookup"><span data-stu-id="ad3ae-106">The **Get-AzDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="ad3ae-107">Il cmdlet restituisce se lo stato del criterio è abilitato e l'ora del giorno in cui è stata impostata la chiusura automatica delle macchine virtuali Lab.</span><span class="sxs-lookup"><span data-stu-id="ad3ae-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="ad3ae-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad3ae-108">EXAMPLES</span></span>

## <span data-ttu-id="ad3ae-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad3ae-109">PARAMETERS</span></span>

### <span data-ttu-id="ad3ae-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3ae-110">-DefaultProfile</span></span>
<span data-ttu-id="ad3ae-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ad3ae-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad3ae-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="ad3ae-112">-LabName</span></span>
<span data-ttu-id="ad3ae-113">Specifica il nome del Lab per cui questo cmdlet ottiene i criteri di arresto automatico.</span><span class="sxs-lookup"><span data-stu-id="ad3ae-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="ad3ae-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad3ae-114">-ResourceGroupName</span></span>
<span data-ttu-id="ad3ae-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="ad3ae-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="ad3ae-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3ae-116">CommonParameters</span></span>
<span data-ttu-id="ad3ae-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad3ae-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3ae-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad3ae-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3ae-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad3ae-119">INPUTS</span></span>

### <span data-ttu-id="ad3ae-120">System. String</span><span class="sxs-lookup"><span data-stu-id="ad3ae-120">System.String</span></span>

## <span data-ttu-id="ad3ae-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad3ae-121">OUTPUTS</span></span>

### <span data-ttu-id="ad3ae-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="ad3ae-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="ad3ae-123">Note</span><span class="sxs-lookup"><span data-stu-id="ad3ae-123">NOTES</span></span>

## <span data-ttu-id="ad3ae-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad3ae-124">RELATED LINKS</span></span>

[<span data-ttu-id="ad3ae-125">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="ad3ae-125">Set-AzDtlAutoShutdownPolicy</span></span>](./Set-AzDtlAutoShutdownPolicy.md)


