---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: f1b5d95397aad24b84462c7e9ceba4a06ba854c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994361"
---
# <span data-ttu-id="b1de8-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="b1de8-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="b1de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1de8-102">SYNOPSIS</span></span>
<span data-ttu-id="b1de8-103">Ottiene i criteri consentiti per le dimensioni delle macchine virtuali di un lab nei laboratori DevTest.</span><span class="sxs-lookup"><span data-stu-id="b1de8-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="b1de8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1de8-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1de8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1de8-105">DESCRIPTION</span></span>
<span data-ttu-id="b1de8-106">Il cmdlet **Get-AzDtlAllowedVMSizesPolicy** ottiene il criterio di dimensioni delle macchine virtuali consentite, che consente di specificare un elenco delle dimensioni di macchine virtuali consentite nel lab.</span><span class="sxs-lookup"><span data-stu-id="b1de8-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="b1de8-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e un elenco di tutte le dimensioni di macchine virtuali consentite impostate nel criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="b1de8-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="b1de8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1de8-108">EXAMPLES</span></span>

## <span data-ttu-id="b1de8-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1de8-109">PARAMETERS</span></span>

### <span data-ttu-id="b1de8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1de8-110">-DefaultProfile</span></span>
<span data-ttu-id="b1de8-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b1de8-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1de8-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="b1de8-112">-LabName</span></span>
<span data-ttu-id="b1de8-113">Specifica il nome del lab per cui questo cmdlet ottiene i criteri per le dimensioni delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b1de8-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="b1de8-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1de8-114">-ResourceGroupName</span></span>
<span data-ttu-id="b1de8-115">Specifica il nome del gruppo di risorse a cui appartiene il laboratorio.</span><span class="sxs-lookup"><span data-stu-id="b1de8-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="b1de8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1de8-116">CommonParameters</span></span>
<span data-ttu-id="b1de8-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1de8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1de8-118">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1de8-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1de8-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1de8-119">INPUTS</span></span>

### <span data-ttu-id="b1de8-120">System.String</span><span class="sxs-lookup"><span data-stu-id="b1de8-120">System.String</span></span>

## <span data-ttu-id="b1de8-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1de8-121">OUTPUTS</span></span>

### <span data-ttu-id="b1de8-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b1de8-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="b1de8-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1de8-123">NOTES</span></span>

## <span data-ttu-id="b1de8-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1de8-124">RELATED LINKS</span></span>

[<span data-ttu-id="b1de8-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="b1de8-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


