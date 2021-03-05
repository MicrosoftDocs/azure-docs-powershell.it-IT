---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 86d8e3bfebe8e87abacc78859dd6e776ff2ccf0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981005"
---
# <span data-ttu-id="3d91f-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="3d91f-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="3d91f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d91f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d91f-103">Ottenere un documento di comando per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3d91f-103">Get a run command document.</span></span>

## <span data-ttu-id="3d91f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d91f-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d91f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3d91f-105">DESCRIPTION</span></span>
<span data-ttu-id="3d91f-106">Ottenere un documento di comando per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3d91f-106">Get a run command document.</span></span>

## <span data-ttu-id="3d91f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d91f-107">EXAMPLES</span></span>

### <span data-ttu-id="3d91f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d91f-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="3d91f-109">Ottiene un documento di comando di esecuzione specifico per 'RunPowerShellScript' in 'westus'.</span><span class="sxs-lookup"><span data-stu-id="3d91f-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="3d91f-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3d91f-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="3d91f-111">Elenca tutti i comandi di esecuzione disponibili in 'westus'.</span><span class="sxs-lookup"><span data-stu-id="3d91f-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="3d91f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d91f-112">PARAMETERS</span></span>

### <span data-ttu-id="3d91f-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="3d91f-113">-CommandId</span></span>
<span data-ttu-id="3d91f-114">ID comando.</span><span class="sxs-lookup"><span data-stu-id="3d91f-114">The command ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d91f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d91f-115">-DefaultProfile</span></span>
<span data-ttu-id="3d91f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d91f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d91f-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3d91f-117">-Location</span></span>
<span data-ttu-id="3d91f-118">Posizione in cui vengono eseguiti i comandi di esecuzione della query.</span><span class="sxs-lookup"><span data-stu-id="3d91f-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="3d91f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d91f-119">CommonParameters</span></span>
<span data-ttu-id="3d91f-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d91f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d91f-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d91f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d91f-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="3d91f-122">INPUTS</span></span>

### <span data-ttu-id="3d91f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3d91f-123">System.String</span></span>

## <span data-ttu-id="3d91f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d91f-124">OUTPUTS</span></span>

### <span data-ttu-id="3d91f-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="3d91f-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="3d91f-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="3d91f-126">NOTES</span></span>

## <span data-ttu-id="3d91f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d91f-127">RELATED LINKS</span></span>
