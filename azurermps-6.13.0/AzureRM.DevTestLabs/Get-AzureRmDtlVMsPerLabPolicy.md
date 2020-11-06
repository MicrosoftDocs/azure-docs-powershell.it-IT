---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3f38c8ace41a1f125a37053f136cd61c597787ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513871"
---
# <span data-ttu-id="363f0-101">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="363f0-101">Get-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="363f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="363f0-102">SYNOPSIS</span></span>
<span data-ttu-id="363f0-103">Ottiene le macchine virtuali per i criteri Lab di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="363f0-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="363f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="363f0-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="363f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="363f0-105">DESCRIPTION</span></span>
<span data-ttu-id="363f0-106">Il cmdlet **Get-AzureRmDtlVMsPerLabPolicy** ottiene le macchine virtuali per i criteri Lab di un Lab, che consente di impostare il numero totale di macchine virtuali consentite in un Lab.</span><span class="sxs-lookup"><span data-stu-id="363f0-106">The **Get-AzureRmDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="363f0-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e il numero totale di macchine virtuali consentite nel Lab impostato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="363f0-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="363f0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="363f0-108">EXAMPLES</span></span>

## <span data-ttu-id="363f0-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="363f0-109">PARAMETERS</span></span>

### <span data-ttu-id="363f0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="363f0-110">-DefaultProfile</span></span>
<span data-ttu-id="363f0-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="363f0-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="363f0-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="363f0-112">-LabName</span></span>
<span data-ttu-id="363f0-113">Specifica il nome del Lab per cui questo cmdlet ottiene le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="363f0-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="363f0-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="363f0-114">-ResourceGroupName</span></span>
<span data-ttu-id="363f0-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="363f0-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="363f0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="363f0-116">CommonParameters</span></span>
<span data-ttu-id="363f0-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="363f0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="363f0-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="363f0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="363f0-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="363f0-119">INPUTS</span></span>

### <span data-ttu-id="363f0-120">System. String</span><span class="sxs-lookup"><span data-stu-id="363f0-120">System.String</span></span>

## <span data-ttu-id="363f0-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="363f0-121">OUTPUTS</span></span>

### <span data-ttu-id="363f0-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="363f0-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="363f0-123">Note</span><span class="sxs-lookup"><span data-stu-id="363f0-123">NOTES</span></span>

## <span data-ttu-id="363f0-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="363f0-124">RELATED LINKS</span></span>

[<span data-ttu-id="363f0-125">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="363f0-125">Set-AzureRmDtlVMsPerLabPolicy</span></span>](./Set-AzureRmDtlVMsPerLabPolicy.md)

