---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
ms.openlocfilehash: d51528cab51e4e6fe6cda428e25965d65c449c4b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866758"
---
# <span data-ttu-id="fd1d6-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="fd1d6-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="fd1d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="fd1d6-103">Documento di comando Get Run.</span><span class="sxs-lookup"><span data-stu-id="fd1d6-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd1d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd1d6-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd1d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd1d6-105">DESCRIPTION</span></span>
<span data-ttu-id="fd1d6-106">Documento di comando Get Run.</span><span class="sxs-lookup"><span data-stu-id="fd1d6-106">Get run command document.</span></span>

## <span data-ttu-id="fd1d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd1d6-107">EXAMPLES</span></span>

### <span data-ttu-id="fd1d6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd1d6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="fd1d6-109">Ottiene un documento di comando di esecuzione specifico per "RunPowerShellScript" in "westus".</span><span class="sxs-lookup"><span data-stu-id="fd1d6-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="fd1d6-110">Get-AzureRmVMRunCommandDocument-posizione $loc</span><span class="sxs-lookup"><span data-stu-id="fd1d6-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="fd1d6-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fd1d6-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="fd1d6-112">Elenca tutti i comandi di esecuzione disponibili in ' westus '.</span><span class="sxs-lookup"><span data-stu-id="fd1d6-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="fd1d6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd1d6-113">PARAMETERS</span></span>

### <span data-ttu-id="fd1d6-114">-CommandID</span><span class="sxs-lookup"><span data-stu-id="fd1d6-114">-CommandId</span></span>
<span data-ttu-id="fd1d6-115">ID comando.</span><span class="sxs-lookup"><span data-stu-id="fd1d6-115">The command id.</span></span>

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

### <span data-ttu-id="fd1d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd1d6-116">-DefaultProfile</span></span>
<span data-ttu-id="fd1d6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd1d6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd1d6-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fd1d6-118">-Location</span></span>
<span data-ttu-id="fd1d6-119">Posizione in cui vengono eseguite le query sui comandi.</span><span class="sxs-lookup"><span data-stu-id="fd1d6-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="fd1d6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd1d6-120">CommonParameters</span></span>
<span data-ttu-id="fd1d6-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd1d6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd1d6-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd1d6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd1d6-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd1d6-123">INPUTS</span></span>

### <span data-ttu-id="fd1d6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fd1d6-124">System.String</span></span>

## <span data-ttu-id="fd1d6-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd1d6-125">OUTPUTS</span></span>

### <span data-ttu-id="fd1d6-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="fd1d6-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="fd1d6-127">Note</span><span class="sxs-lookup"><span data-stu-id="fd1d6-127">NOTES</span></span>

## <span data-ttu-id="fd1d6-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd1d6-128">RELATED LINKS</span></span>

