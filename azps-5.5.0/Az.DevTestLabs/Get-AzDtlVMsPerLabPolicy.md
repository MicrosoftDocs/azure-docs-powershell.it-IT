---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 29d887639dd88f85a24144a4482c40c2b7626c7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200439"
---
# <span data-ttu-id="d2c3e-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d2c3e-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="d2c3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c3e-103">Recupera le macchine virtuali per i criteri lab di un lab nei laboratori DevTest.</span><span class="sxs-lookup"><span data-stu-id="d2c3e-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="d2c3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2c3e-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2c3e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d2c3e-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c3e-106">Il cmdlet **Get-AzDtlVMsPerLabPolicy** ottiene le macchine virtuali per criterio lab di un lab, che consente di impostare il numero totale di macchine virtuali consentite in un lab.</span><span class="sxs-lookup"><span data-stu-id="d2c3e-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="d2c3e-107">Il cmdlet restituisce lo stato abilitato o disabilitato dei criteri e il numero totale di macchine virtuali consentite nel lab che sono state impostate nei criteri.</span><span class="sxs-lookup"><span data-stu-id="d2c3e-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="d2c3e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2c3e-108">EXAMPLES</span></span>

## <span data-ttu-id="d2c3e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2c3e-109">PARAMETERS</span></span>

### <span data-ttu-id="d2c3e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c3e-110">-DefaultProfile</span></span>
<span data-ttu-id="d2c3e-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d2c3e-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2c3e-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="d2c3e-112">-LabName</span></span>
<span data-ttu-id="d2c3e-113">Specifica il nome del lab per cui questo cmdlet ottiene le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="d2c3e-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="d2c3e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c3e-114">-ResourceGroupName</span></span>
<span data-ttu-id="d2c3e-115">Specifica il nome del gruppo di risorse a cui appartiene il laboratorio.</span><span class="sxs-lookup"><span data-stu-id="d2c3e-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d2c3e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c3e-116">CommonParameters</span></span>
<span data-ttu-id="d2c3e-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c3e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c3e-118">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c3e-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c3e-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="d2c3e-119">INPUTS</span></span>

### <span data-ttu-id="d2c3e-120">System.String</span><span class="sxs-lookup"><span data-stu-id="d2c3e-120">System.String</span></span>

## <span data-ttu-id="d2c3e-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2c3e-121">OUTPUTS</span></span>

### <span data-ttu-id="d2c3e-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d2c3e-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="d2c3e-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="d2c3e-123">NOTES</span></span>

## <span data-ttu-id="d2c3e-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2c3e-124">RELATED LINKS</span></span>

[<span data-ttu-id="d2c3e-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="d2c3e-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


