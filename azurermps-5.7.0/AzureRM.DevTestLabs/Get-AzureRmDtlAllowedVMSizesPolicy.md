---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 25b3f15b6a71b54cbcab1a53f793a32da8b2173a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685996"
---
# <span data-ttu-id="5f2c2-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="5f2c2-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="5f2c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="5f2c2-103">Ottiene i criteri di dimensioni della macchina virtuale consentiti di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="5f2c2-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f2c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f2c2-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f2c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f2c2-105">DESCRIPTION</span></span>
<span data-ttu-id="5f2c2-106">Il cmdlet **Get-AzureRmDtlAllowedVMSizesPolicy** ottiene i criteri di dimensioni della macchina virtuale consentiti, che consente di specificare un elenco delle dimensioni della macchina virtuale consentite in Lab.</span><span class="sxs-lookup"><span data-stu-id="5f2c2-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="5f2c2-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e un elenco di tutte le dimensioni della macchina virtuale consentite impostate nei criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="5f2c2-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="5f2c2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f2c2-108">EXAMPLES</span></span>

## <span data-ttu-id="5f2c2-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f2c2-109">PARAMETERS</span></span>

### <span data-ttu-id="5f2c2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f2c2-110">-DefaultProfile</span></span>
<span data-ttu-id="5f2c2-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5f2c2-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f2c2-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="5f2c2-112">-LabName</span></span>
<span data-ttu-id="5f2c2-113">Specifica il nome del Lab per il quale questo cmdlet ottiene i criteri per le dimensioni delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="5f2c2-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="5f2c2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f2c2-114">-ResourceGroupName</span></span>
<span data-ttu-id="5f2c2-115">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="5f2c2-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="5f2c2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f2c2-116">CommonParameters</span></span>
<span data-ttu-id="5f2c2-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f2c2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f2c2-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f2c2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f2c2-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f2c2-119">INPUTS</span></span>

### <span data-ttu-id="5f2c2-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5f2c2-120">None</span></span>
<span data-ttu-id="5f2c2-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5f2c2-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f2c2-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f2c2-122">OUTPUTS</span></span>

### <span data-ttu-id="5f2c2-123">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5f2c2-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="5f2c2-124">Questo cmdlet restituisce i criteri che specificano l'elenco delle dimensioni della macchina virtuale consentite in Lab.</span><span class="sxs-lookup"><span data-stu-id="5f2c2-124">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="5f2c2-125">Note</span><span class="sxs-lookup"><span data-stu-id="5f2c2-125">NOTES</span></span>

## <span data-ttu-id="5f2c2-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f2c2-126">RELATED LINKS</span></span>

[<span data-ttu-id="5f2c2-127">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="5f2c2-127">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="5f2c2-128">Cmdlet di Lab Development test di Azure</span><span class="sxs-lookup"><span data-stu-id="5f2c2-128">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)


