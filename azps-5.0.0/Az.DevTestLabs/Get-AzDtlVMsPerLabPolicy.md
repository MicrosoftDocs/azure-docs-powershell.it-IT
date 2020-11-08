---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 29d887639dd88f85a24144a4482c40c2b7626c7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193508"
---
# <span data-ttu-id="d5cfe-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d5cfe-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="d5cfe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5cfe-102">SYNOPSIS</span></span>
<span data-ttu-id="d5cfe-103">Ottiene le macchine virtuali per i criteri Lab di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="d5cfe-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="d5cfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5cfe-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5cfe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5cfe-105">DESCRIPTION</span></span>
<span data-ttu-id="d5cfe-106">Il cmdlet **Get-AzDtlVMsPerLabPolicy** ottiene le macchine virtuali per i criteri Lab di un Lab, che consente di impostare il numero totale di macchine virtuali consentite in un Lab.</span><span class="sxs-lookup"><span data-stu-id="d5cfe-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="d5cfe-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e il numero totale di macchine virtuali consentite nel Lab impostato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="d5cfe-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="d5cfe-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5cfe-108">EXAMPLES</span></span>

## <span data-ttu-id="d5cfe-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5cfe-109">PARAMETERS</span></span>

### <span data-ttu-id="d5cfe-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5cfe-110">-DefaultProfile</span></span>
<span data-ttu-id="d5cfe-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d5cfe-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5cfe-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="d5cfe-112">-LabName</span></span>
<span data-ttu-id="d5cfe-113">Specifica il nome del Lab per cui questo cmdlet ottiene le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="d5cfe-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="d5cfe-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5cfe-114">-ResourceGroupName</span></span>
<span data-ttu-id="d5cfe-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="d5cfe-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d5cfe-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5cfe-116">CommonParameters</span></span>
<span data-ttu-id="d5cfe-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5cfe-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5cfe-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5cfe-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5cfe-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5cfe-119">INPUTS</span></span>

### <span data-ttu-id="d5cfe-120">System. String</span><span class="sxs-lookup"><span data-stu-id="d5cfe-120">System.String</span></span>

## <span data-ttu-id="d5cfe-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5cfe-121">OUTPUTS</span></span>

### <span data-ttu-id="d5cfe-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d5cfe-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="d5cfe-123">Note</span><span class="sxs-lookup"><span data-stu-id="d5cfe-123">NOTES</span></span>

## <span data-ttu-id="d5cfe-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5cfe-124">RELATED LINKS</span></span>

[<span data-ttu-id="d5cfe-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d5cfe-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)

