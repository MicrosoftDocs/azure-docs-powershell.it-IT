---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: b0bb5d90fe304d2663671fdc8a2277d2adb18322
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975965"
---
# <span data-ttu-id="de6a9-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="de6a9-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="de6a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de6a9-102">SYNOPSIS</span></span>
<span data-ttu-id="de6a9-103">Riavvia un'istanza del server analysis services nell'ambiente attualmente connesso come specificato nel comando Add-AzAnalysisServicesAccount></span><span class="sxs-lookup"><span data-stu-id="de6a9-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="de6a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de6a9-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de6a9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="de6a9-105">DESCRIPTION</span></span>
<span data-ttu-id="de6a9-106">Il cmdlet Restart-AzAnalysisServicesInstance riavvia un'istanza del server di Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="de6a9-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="de6a9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de6a9-107">EXAMPLES</span></span>

### <span data-ttu-id="de6a9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de6a9-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="de6a9-109">Questo comando riavvierà il server 'testserver' nell'ambiente specificato nel comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="de6a9-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="de6a9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de6a9-110">PARAMETERS</span></span>

### <span data-ttu-id="de6a9-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="de6a9-111">-Instance</span></span>
<span data-ttu-id="de6a9-112">Nome dell'istanza del server Analysis Services da riavviare</span><span class="sxs-lookup"><span data-stu-id="de6a9-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de6a9-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de6a9-113">-PassThru</span></span>
<span data-ttu-id="de6a9-114">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="de6a9-114">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6a9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de6a9-115">-Confirm</span></span>
<span data-ttu-id="de6a9-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de6a9-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6a9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de6a9-117">-WhatIf</span></span>
<span data-ttu-id="de6a9-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de6a9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de6a9-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de6a9-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6a9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6a9-120">CommonParameters</span></span>
<span data-ttu-id="de6a9-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de6a9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6a9-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de6a9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6a9-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="de6a9-123">INPUTS</span></span>

### <span data-ttu-id="de6a9-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="de6a9-124">None</span></span>

## <span data-ttu-id="de6a9-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de6a9-125">OUTPUTS</span></span>

### <span data-ttu-id="de6a9-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de6a9-126">System.Boolean</span></span>

## <span data-ttu-id="de6a9-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="de6a9-127">NOTES</span></span>
<span data-ttu-id="de6a9-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="de6a9-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="de6a9-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de6a9-129">RELATED LINKS</span></span>
