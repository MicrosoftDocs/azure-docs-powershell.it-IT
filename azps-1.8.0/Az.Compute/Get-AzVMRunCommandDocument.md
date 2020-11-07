---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 3b66cdc6574397de7d43dfef0677a5ddac772a31
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684802"
---
# <span data-ttu-id="83c25-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="83c25-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="83c25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83c25-102">SYNOPSIS</span></span>
<span data-ttu-id="83c25-103">Ottenere un documento di comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="83c25-103">Get a run command document.</span></span>

## <span data-ttu-id="83c25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83c25-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83c25-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83c25-105">DESCRIPTION</span></span>
<span data-ttu-id="83c25-106">Ottenere un documento di comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="83c25-106">Get a run command document.</span></span>

## <span data-ttu-id="83c25-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83c25-107">EXAMPLES</span></span>

### <span data-ttu-id="83c25-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="83c25-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="83c25-109">Ottiene un documento di comando di esecuzione specifico per "RunPowerShellScript" in "westus".</span><span class="sxs-lookup"><span data-stu-id="83c25-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="83c25-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="83c25-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="83c25-111">Elenca tutti i comandi di esecuzione disponibili in ' westus '.</span><span class="sxs-lookup"><span data-stu-id="83c25-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="83c25-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83c25-112">PARAMETERS</span></span>

### <span data-ttu-id="83c25-113">-CommandID</span><span class="sxs-lookup"><span data-stu-id="83c25-113">-CommandId</span></span>
<span data-ttu-id="83c25-114">ID comando.</span><span class="sxs-lookup"><span data-stu-id="83c25-114">The command ID.</span></span>

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

### <span data-ttu-id="83c25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c25-115">-DefaultProfile</span></span>
<span data-ttu-id="83c25-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83c25-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83c25-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="83c25-117">-Location</span></span>
<span data-ttu-id="83c25-118">Posizione in cui vengono eseguite le query sui comandi.</span><span class="sxs-lookup"><span data-stu-id="83c25-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="83c25-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c25-119">CommonParameters</span></span>
<span data-ttu-id="83c25-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c25-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c25-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83c25-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c25-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83c25-122">INPUTS</span></span>

### <span data-ttu-id="83c25-123">System. String</span><span class="sxs-lookup"><span data-stu-id="83c25-123">System.String</span></span>

## <span data-ttu-id="83c25-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83c25-124">OUTPUTS</span></span>

### <span data-ttu-id="83c25-125">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="83c25-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="83c25-126">Note</span><span class="sxs-lookup"><span data-stu-id="83c25-126">NOTES</span></span>

## <span data-ttu-id="83c25-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83c25-127">RELATED LINKS</span></span>
