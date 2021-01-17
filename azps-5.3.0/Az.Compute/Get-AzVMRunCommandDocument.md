---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488464"
---
# <span data-ttu-id="b2918-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="b2918-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="b2918-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2918-102">SYNOPSIS</span></span>
<span data-ttu-id="b2918-103">Ottenere un documento di comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="b2918-103">Get a run command document.</span></span>

## <span data-ttu-id="b2918-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2918-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2918-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2918-105">DESCRIPTION</span></span>
<span data-ttu-id="b2918-106">Ottenere un documento di comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="b2918-106">Get a run command document.</span></span>

## <span data-ttu-id="b2918-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2918-107">EXAMPLES</span></span>

### <span data-ttu-id="b2918-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b2918-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="b2918-109">Ottiene un documento di comando di esecuzione specifico per "RunPowerShellScript" in "westus".</span><span class="sxs-lookup"><span data-stu-id="b2918-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="b2918-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b2918-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="b2918-111">Elenca tutti i comandi di esecuzione disponibili in ' westus '.</span><span class="sxs-lookup"><span data-stu-id="b2918-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="b2918-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2918-112">PARAMETERS</span></span>

### <span data-ttu-id="b2918-113">-CommandID</span><span class="sxs-lookup"><span data-stu-id="b2918-113">-CommandId</span></span>
<span data-ttu-id="b2918-114">ID comando.</span><span class="sxs-lookup"><span data-stu-id="b2918-114">The command ID.</span></span>

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

### <span data-ttu-id="b2918-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2918-115">-DefaultProfile</span></span>
<span data-ttu-id="b2918-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2918-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2918-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b2918-117">-Location</span></span>
<span data-ttu-id="b2918-118">Posizione in cui vengono eseguite le query sui comandi.</span><span class="sxs-lookup"><span data-stu-id="b2918-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="b2918-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2918-119">CommonParameters</span></span>
<span data-ttu-id="b2918-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2918-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2918-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2918-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2918-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2918-122">INPUTS</span></span>

### <span data-ttu-id="b2918-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b2918-123">System.String</span></span>

## <span data-ttu-id="b2918-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2918-124">OUTPUTS</span></span>

### <span data-ttu-id="b2918-125">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="b2918-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="b2918-126">Note</span><span class="sxs-lookup"><span data-stu-id="b2918-126">NOTES</span></span>

## <span data-ttu-id="b2918-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2918-127">RELATED LINKS</span></span>
