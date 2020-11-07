---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 45d051e5fc2fe750f58dc6400a037960b7eb9c7c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863725"
---
# <span data-ttu-id="01939-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="01939-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="01939-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01939-102">SYNOPSIS</span></span>
<span data-ttu-id="01939-103">Documento di comando Get Run.</span><span class="sxs-lookup"><span data-stu-id="01939-103">Get run command document.</span></span>

## <span data-ttu-id="01939-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01939-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01939-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01939-105">DESCRIPTION</span></span>
<span data-ttu-id="01939-106">Documento di comando Get Run.</span><span class="sxs-lookup"><span data-stu-id="01939-106">Get run command document.</span></span>

## <span data-ttu-id="01939-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01939-107">EXAMPLES</span></span>

### <span data-ttu-id="01939-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="01939-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="01939-109">Ottiene un documento di comando di esecuzione specifico per "RunPowerShellScript" in "westus".</span><span class="sxs-lookup"><span data-stu-id="01939-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="01939-110">Get-AzVMRunCommandDocument-posizione $loc</span><span class="sxs-lookup"><span data-stu-id="01939-110">Get-AzVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="01939-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="01939-111">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="01939-112">Elenca tutti i comandi di esecuzione disponibili in ' westus '.</span><span class="sxs-lookup"><span data-stu-id="01939-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="01939-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01939-113">PARAMETERS</span></span>

### <span data-ttu-id="01939-114">-CommandID</span><span class="sxs-lookup"><span data-stu-id="01939-114">-CommandId</span></span>
<span data-ttu-id="01939-115">ID comando.</span><span class="sxs-lookup"><span data-stu-id="01939-115">The command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01939-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01939-116">-DefaultProfile</span></span>
<span data-ttu-id="01939-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01939-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01939-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="01939-118">-Location</span></span>
<span data-ttu-id="01939-119">Posizione in cui vengono eseguite le query sui comandi.</span><span class="sxs-lookup"><span data-stu-id="01939-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="01939-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01939-120">CommonParameters</span></span>
<span data-ttu-id="01939-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01939-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01939-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01939-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01939-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01939-123">INPUTS</span></span>

### <span data-ttu-id="01939-124">System. String</span><span class="sxs-lookup"><span data-stu-id="01939-124">System.String</span></span>

## <span data-ttu-id="01939-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01939-125">OUTPUTS</span></span>

### <span data-ttu-id="01939-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="01939-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="01939-127">Note</span><span class="sxs-lookup"><span data-stu-id="01939-127">NOTES</span></span>

## <span data-ttu-id="01939-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01939-128">RELATED LINKS</span></span>

