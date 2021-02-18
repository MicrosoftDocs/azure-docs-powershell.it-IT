---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200438"
---
# <span data-ttu-id="c06a1-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="c06a1-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="c06a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c06a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c06a1-103">Recupera le macchine virtuali per criterio utente di un lab nei laboratori DevTest.</span><span class="sxs-lookup"><span data-stu-id="c06a1-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="c06a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c06a1-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c06a1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c06a1-105">DESCRIPTION</span></span>
<span data-ttu-id="c06a1-106">Il cmdlet **Get-AzDtlVMsPerUserPolicy** ottiene le macchine virtuali per criterio utente di un lab, che consente di impostare il numero massimo di macchine virtuali consentite per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="c06a1-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="c06a1-107">Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e il numero massimo di macchine virtuali consentito per ogni utente che è stato impostato nel criterio.</span><span class="sxs-lookup"><span data-stu-id="c06a1-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="c06a1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c06a1-108">EXAMPLES</span></span>

## <span data-ttu-id="c06a1-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c06a1-109">PARAMETERS</span></span>

### <span data-ttu-id="c06a1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06a1-110">-DefaultProfile</span></span>
<span data-ttu-id="c06a1-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="c06a1-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c06a1-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="c06a1-112">-LabName</span></span>
<span data-ttu-id="c06a1-113">Specifica il nome del lab per cui questo cmdlet ottiene la macchina virtuale per ogni criterio utente.</span><span class="sxs-lookup"><span data-stu-id="c06a1-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="c06a1-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c06a1-114">-ResourceGroupName</span></span>
<span data-ttu-id="c06a1-115">Specifica il nome del gruppo di risorse a cui appartiene il laboratorio.</span><span class="sxs-lookup"><span data-stu-id="c06a1-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="c06a1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06a1-116">CommonParameters</span></span>
<span data-ttu-id="c06a1-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c06a1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06a1-118">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c06a1-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06a1-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="c06a1-119">INPUTS</span></span>

### <span data-ttu-id="c06a1-120">System.String</span><span class="sxs-lookup"><span data-stu-id="c06a1-120">System.String</span></span>

## <span data-ttu-id="c06a1-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c06a1-121">OUTPUTS</span></span>

### <span data-ttu-id="c06a1-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c06a1-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="c06a1-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="c06a1-123">NOTES</span></span>

## <span data-ttu-id="c06a1-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c06a1-124">RELATED LINKS</span></span>

[<span data-ttu-id="c06a1-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="c06a1-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


