---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020347"
---
# <span data-ttu-id="40270-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="40270-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="40270-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40270-102">SYNOPSIS</span></span>
<span data-ttu-id="40270-103">Ottiene i criteri per gli utenti delle macchine virtuali di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="40270-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="40270-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40270-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40270-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40270-105">DESCRIPTION</span></span>
<span data-ttu-id="40270-106">Il cmdlet **Get-AzDtlVMsPerUserPolicy** ottiene le macchine virtuali per i criteri utente di un Lab, che consente di impostare il numero massimo di macchine virtuali consentite per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="40270-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="40270-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e il numero massimo di macchine virtuali consentite per ogni utente impostato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="40270-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="40270-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40270-108">EXAMPLES</span></span>

## <span data-ttu-id="40270-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40270-109">PARAMETERS</span></span>

### <span data-ttu-id="40270-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40270-110">-DefaultProfile</span></span>
<span data-ttu-id="40270-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="40270-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40270-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="40270-112">-LabName</span></span>
<span data-ttu-id="40270-113">Specifica il nome del Lab per cui questo cmdlet ottiene il criterio per utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="40270-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="40270-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40270-114">-ResourceGroupName</span></span>
<span data-ttu-id="40270-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="40270-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="40270-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40270-116">CommonParameters</span></span>
<span data-ttu-id="40270-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40270-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40270-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40270-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40270-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40270-119">INPUTS</span></span>

### <span data-ttu-id="40270-120">System. String</span><span class="sxs-lookup"><span data-stu-id="40270-120">System.String</span></span>

## <span data-ttu-id="40270-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40270-121">OUTPUTS</span></span>

### <span data-ttu-id="40270-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="40270-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="40270-123">Note</span><span class="sxs-lookup"><span data-stu-id="40270-123">NOTES</span></span>

## <span data-ttu-id="40270-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40270-124">RELATED LINKS</span></span>

[<span data-ttu-id="40270-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="40270-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


