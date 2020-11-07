---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: ae003c3c523c17db9c486edaa68d7e0991b0e6d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519189"
---
# <span data-ttu-id="cb7de-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="cb7de-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="cb7de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb7de-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7de-103">Ottiene i criteri di dimensioni della macchina virtuale consentiti di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="cb7de-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb7de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb7de-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb7de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb7de-105">DESCRIPTION</span></span>
<span data-ttu-id="cb7de-106">Il cmdlet **Get-AzureRmDtlAllowedVMSizesPolicy** ottiene i criteri di dimensioni della macchina virtuale consentiti, che consente di specificare un elenco delle dimensioni della macchina virtuale consentite in Lab.</span><span class="sxs-lookup"><span data-stu-id="cb7de-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="cb7de-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e un elenco di tutte le dimensioni della macchina virtuale consentite impostate nei criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="cb7de-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="cb7de-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb7de-108">EXAMPLES</span></span>

## <span data-ttu-id="cb7de-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb7de-109">PARAMETERS</span></span>

### <span data-ttu-id="cb7de-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="cb7de-110">-LabName</span></span>
<span data-ttu-id="cb7de-111">Specifica il nome del Lab per il quale questo cmdlet ottiene i criteri per le dimensioni delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="cb7de-111">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="cb7de-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb7de-112">-ResourceGroupName</span></span>
<span data-ttu-id="cb7de-113">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="cb7de-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="cb7de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb7de-114">-DefaultProfile</span></span>
<span data-ttu-id="cb7de-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb7de-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb7de-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7de-116">CommonParameters</span></span>
<span data-ttu-id="cb7de-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb7de-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7de-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb7de-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7de-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb7de-119">INPUTS</span></span>

## <span data-ttu-id="cb7de-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb7de-120">OUTPUTS</span></span>

### <span data-ttu-id="cb7de-121">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="cb7de-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="cb7de-122">Questo cmdlet restituisce i criteri che specificano l'elenco delle dimensioni della macchina virtuale consentite in Lab.</span><span class="sxs-lookup"><span data-stu-id="cb7de-122">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="cb7de-123">Note</span><span class="sxs-lookup"><span data-stu-id="cb7de-123">NOTES</span></span>

## <span data-ttu-id="cb7de-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb7de-124">RELATED LINKS</span></span>

[<span data-ttu-id="cb7de-125">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="cb7de-125">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="cb7de-126">Cmdlet di Lab Development test di Azure</span><span class="sxs-lookup"><span data-stu-id="cb7de-126">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)

