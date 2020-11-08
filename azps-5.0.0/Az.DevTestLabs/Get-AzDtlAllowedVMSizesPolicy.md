---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193517"
---
# <span data-ttu-id="2e62f-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="2e62f-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="2e62f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e62f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e62f-103">Ottiene i criteri di dimensioni della macchina virtuale consentiti di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="2e62f-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="2e62f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e62f-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e62f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e62f-105">DESCRIPTION</span></span>
<span data-ttu-id="2e62f-106">Il cmdlet **Get-AzDtlAllowedVMSizesPolicy** ottiene i criteri di dimensioni della macchina virtuale consentiti, che consente di specificare un elenco delle dimensioni della macchina virtuale consentite in Lab.</span><span class="sxs-lookup"><span data-stu-id="2e62f-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="2e62f-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e un elenco di tutte le dimensioni della macchina virtuale consentite impostate nei criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="2e62f-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="2e62f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e62f-108">EXAMPLES</span></span>

## <span data-ttu-id="2e62f-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e62f-109">PARAMETERS</span></span>

### <span data-ttu-id="2e62f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e62f-110">-DefaultProfile</span></span>
<span data-ttu-id="2e62f-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2e62f-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e62f-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="2e62f-112">-LabName</span></span>
<span data-ttu-id="2e62f-113">Specifica il nome del Lab per il quale questo cmdlet ottiene i criteri per le dimensioni delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="2e62f-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="2e62f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e62f-114">-ResourceGroupName</span></span>
<span data-ttu-id="2e62f-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="2e62f-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="2e62f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e62f-116">CommonParameters</span></span>
<span data-ttu-id="2e62f-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e62f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e62f-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e62f-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e62f-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e62f-119">INPUTS</span></span>

### <span data-ttu-id="2e62f-120">System. String</span><span class="sxs-lookup"><span data-stu-id="2e62f-120">System.String</span></span>

## <span data-ttu-id="2e62f-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e62f-121">OUTPUTS</span></span>

### <span data-ttu-id="2e62f-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="2e62f-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="2e62f-123">Note</span><span class="sxs-lookup"><span data-stu-id="2e62f-123">NOTES</span></span>

## <span data-ttu-id="2e62f-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e62f-124">RELATED LINKS</span></span>

[<span data-ttu-id="2e62f-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="2e62f-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)

