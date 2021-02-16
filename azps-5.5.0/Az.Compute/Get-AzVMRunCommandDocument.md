---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199286"
---
# <span data-ttu-id="94798-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="94798-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="94798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94798-102">SYNOPSIS</span></span>
<span data-ttu-id="94798-103">Ottenere un documento di comando per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="94798-103">Get a run command document.</span></span>

## <span data-ttu-id="94798-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94798-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94798-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94798-105">DESCRIPTION</span></span>
<span data-ttu-id="94798-106">Ottenere un documento di comando per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="94798-106">Get a run command document.</span></span>

## <span data-ttu-id="94798-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94798-107">EXAMPLES</span></span>

### <span data-ttu-id="94798-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94798-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="94798-109">Ottiene un documento di comando di esecuzione specifico per 'RunPowerShellScript' in 'westus'.</span><span class="sxs-lookup"><span data-stu-id="94798-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="94798-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="94798-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="94798-111">Elenca tutti i comandi di esecuzione disponibili in 'westus'.</span><span class="sxs-lookup"><span data-stu-id="94798-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="94798-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94798-112">PARAMETERS</span></span>

### <span data-ttu-id="94798-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="94798-113">-CommandId</span></span>
<span data-ttu-id="94798-114">ID comando.</span><span class="sxs-lookup"><span data-stu-id="94798-114">The command ID.</span></span>

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

### <span data-ttu-id="94798-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94798-115">-DefaultProfile</span></span>
<span data-ttu-id="94798-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94798-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94798-117">-Location</span><span class="sxs-lookup"><span data-stu-id="94798-117">-Location</span></span>
<span data-ttu-id="94798-118">Posizione in cui vengono eseguiti i comandi di esecuzione della query.</span><span class="sxs-lookup"><span data-stu-id="94798-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="94798-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94798-119">CommonParameters</span></span>
<span data-ttu-id="94798-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94798-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94798-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94798-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94798-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="94798-122">INPUTS</span></span>

### <span data-ttu-id="94798-123">System.String</span><span class="sxs-lookup"><span data-stu-id="94798-123">System.String</span></span>

## <span data-ttu-id="94798-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94798-124">OUTPUTS</span></span>

### <span data-ttu-id="94798-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="94798-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="94798-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="94798-126">NOTES</span></span>

## <span data-ttu-id="94798-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94798-127">RELATED LINKS</span></span>
