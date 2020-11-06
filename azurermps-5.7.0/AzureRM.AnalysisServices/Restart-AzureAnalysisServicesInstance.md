---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 0a89ee592e6f6f6d4d9e56df6d7e4df32b010524
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515847"
---
# <span data-ttu-id="43ac7-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="43ac7-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="43ac7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="43ac7-103">Riavvia un'istanza del server di Analysis Services nell'ambiente attualmente connesso, come specificato in comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="43ac7-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43ac7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43ac7-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="43ac7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43ac7-105">DESCRIPTION</span></span>
<span data-ttu-id="43ac7-106">Il cmdlet Restart-AzureAnalysisServicesInstance riavvia un'istanza di Azure Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="43ac7-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="43ac7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43ac7-107">EXAMPLES</span></span>

### <span data-ttu-id="43ac7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="43ac7-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="43ac7-109">Questo comando Riavvia il server "TestServer" nell'ambiente specificato nel comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="43ac7-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="43ac7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43ac7-110">PARAMETERS</span></span>

### <span data-ttu-id="43ac7-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="43ac7-111">-Instance</span></span>
<span data-ttu-id="43ac7-112">Nome dell'istanza del server Analysis Services da riavviare</span><span class="sxs-lookup"><span data-stu-id="43ac7-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ac7-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43ac7-113">-PassThru</span></span>
<span data-ttu-id="43ac7-114">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="43ac7-114">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ac7-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43ac7-115">-Confirm</span></span>
<span data-ttu-id="43ac7-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ac7-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ac7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ac7-117">-WhatIf</span></span>
<span data-ttu-id="43ac7-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43ac7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ac7-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43ac7-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="43ac7-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43ac7-120">INPUTS</span></span>

### <span data-ttu-id="43ac7-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="43ac7-121">None</span></span>
<span data-ttu-id="43ac7-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="43ac7-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43ac7-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43ac7-123">OUTPUTS</span></span>

### <span data-ttu-id="43ac7-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43ac7-124">System.Boolean</span></span>

## <span data-ttu-id="43ac7-125">Note</span><span class="sxs-lookup"><span data-stu-id="43ac7-125">NOTES</span></span>
<span data-ttu-id="43ac7-126">Alias: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="43ac7-126">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="43ac7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43ac7-127">RELATED LINKS</span></span>

