---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479079"
---
# <span data-ttu-id="5b264-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="5b264-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="5b264-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b264-102">SYNOPSIS</span></span>
<span data-ttu-id="5b264-103">Riavvia un'istanza del server di Analysis Services nell'ambiente attualmente connesso, come specificato in comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5b264-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="5b264-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b264-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b264-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b264-105">DESCRIPTION</span></span>
<span data-ttu-id="5b264-106">Il cmdlet Restart-AzAnalysisServicesInstance riavvia un'istanza di Azure Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="5b264-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="5b264-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b264-107">EXAMPLES</span></span>

### <span data-ttu-id="5b264-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5b264-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="5b264-109">Questo comando Riavvia il server "TestServer" nell'ambiente specificato nel comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5b264-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="5b264-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b264-110">PARAMETERS</span></span>

### <span data-ttu-id="5b264-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="5b264-111">-Instance</span></span>
<span data-ttu-id="5b264-112">Nome dell'istanza del server Analysis Services da riavviare</span><span class="sxs-lookup"><span data-stu-id="5b264-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="5b264-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b264-113">-PassThru</span></span>
<span data-ttu-id="5b264-114">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="5b264-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5b264-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b264-115">-Confirm</span></span>
<span data-ttu-id="5b264-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b264-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b264-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b264-117">-WhatIf</span></span>
<span data-ttu-id="5b264-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b264-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b264-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b264-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b264-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b264-120">CommonParameters</span></span>
<span data-ttu-id="5b264-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b264-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b264-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b264-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b264-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b264-123">INPUTS</span></span>

### <span data-ttu-id="5b264-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5b264-124">None</span></span>

## <span data-ttu-id="5b264-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b264-125">OUTPUTS</span></span>

### <span data-ttu-id="5b264-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b264-126">System.Boolean</span></span>

## <span data-ttu-id="5b264-127">Note</span><span class="sxs-lookup"><span data-stu-id="5b264-127">NOTES</span></span>
<span data-ttu-id="5b264-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="5b264-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="5b264-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b264-129">RELATED LINKS</span></span>
