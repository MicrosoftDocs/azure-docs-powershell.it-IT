---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 83b061c646d8d6f75689d6a67fe163c43456edb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514352"
---
# <span data-ttu-id="d75f4-101">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d75f4-101">Get-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="d75f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d75f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d75f4-103">Ottiene le macchine virtuali per i criteri Lab di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="d75f4-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d75f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d75f4-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d75f4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d75f4-105">DESCRIPTION</span></span>
<span data-ttu-id="d75f4-106">Il cmdlet **Get-AzureRmDtlVMsPerLabPolicy** ottiene le macchine virtuali per i criteri Lab di un Lab, che consente di impostare il numero totale di macchine virtuali consentite in un Lab.</span><span class="sxs-lookup"><span data-stu-id="d75f4-106">The **Get-AzureRmDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="d75f4-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e il numero totale di macchine virtuali consentite nel Lab impostato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="d75f4-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="d75f4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d75f4-108">EXAMPLES</span></span>

## <span data-ttu-id="d75f4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d75f4-109">PARAMETERS</span></span>

### <span data-ttu-id="d75f4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d75f4-110">-DefaultProfile</span></span>
<span data-ttu-id="d75f4-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d75f4-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d75f4-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="d75f4-112">-LabName</span></span>
<span data-ttu-id="d75f4-113">Specifica il nome del Lab per cui questo cmdlet ottiene le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="d75f4-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="d75f4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d75f4-114">-ResourceGroupName</span></span>
<span data-ttu-id="d75f4-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="d75f4-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d75f4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d75f4-116">CommonParameters</span></span>
<span data-ttu-id="d75f4-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d75f4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d75f4-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d75f4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d75f4-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d75f4-119">INPUTS</span></span>

### <span data-ttu-id="d75f4-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d75f4-120">None</span></span>
<span data-ttu-id="d75f4-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d75f4-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d75f4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d75f4-122">OUTPUTS</span></span>

### <span data-ttu-id="d75f4-123">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d75f4-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="d75f4-124">Questo cmdlet restituisce il criterio che specifica il numero massimo di macchine virtuali che possono essere create in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="d75f4-124">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="d75f4-125">Note</span><span class="sxs-lookup"><span data-stu-id="d75f4-125">NOTES</span></span>

## <span data-ttu-id="d75f4-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d75f4-126">RELATED LINKS</span></span>

[<span data-ttu-id="d75f4-127">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d75f4-127">Set-AzureRmDtlVMsPerLabPolicy</span></span>](./Set-AzureRmDtlVMsPerLabPolicy.md)


