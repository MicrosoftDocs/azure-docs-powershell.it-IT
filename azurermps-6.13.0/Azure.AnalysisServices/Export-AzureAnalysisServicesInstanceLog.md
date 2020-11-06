---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: dad0e14b72c256706456ed3c923b966323fd7dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512092"
---
# <span data-ttu-id="2fdff-101">Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="2fdff-101">Export-AzureAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="2fdff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fdff-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdff-103">Esporta un log da un'istanza del server di Analysis Services nell'ambiente attualmente connesso, come specificato nel comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2fdff-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fdff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fdff-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog -Instance <String> -OutputPath <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fdff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fdff-105">DESCRIPTION</span></span>
<span data-ttu-id="2fdff-106">Il cmdlet Export-AzureAnalysisServicesInstance Esporta il log da un'istanza di Azure Analysis Services server a file</span><span class="sxs-lookup"><span data-stu-id="2fdff-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="2fdff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fdff-107">EXAMPLES</span></span>

### <span data-ttu-id="2fdff-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2fdff-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="2fdff-109">Questo comando esporterà il log dal server "TestServer" nell'ambiente specificato nel comando Add-AzureAnalysisServicesAccount e lo salverà in file specificato in OutputPath "C:\path\to\log\testserver.log"</span><span class="sxs-lookup"><span data-stu-id="2fdff-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="2fdff-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fdff-110">PARAMETERS</span></span>

### <span data-ttu-id="2fdff-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2fdff-111">-Force</span></span>
<span data-ttu-id="2fdff-112">Sovrascrivere il file se esiste senza chiedere</span><span class="sxs-lookup"><span data-stu-id="2fdff-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="2fdff-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="2fdff-113">-Instance</span></span>
<span data-ttu-id="2fdff-114">Nome dell'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2fdff-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdff-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="2fdff-115">-OutputPath</span></span>
<span data-ttu-id="2fdff-116">Percorso di output del file per esportare il log</span><span class="sxs-lookup"><span data-stu-id="2fdff-116">Output path to file to export log</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdff-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2fdff-117">-Confirm</span></span>
<span data-ttu-id="2fdff-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fdff-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fdff-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fdff-119">-WhatIf</span></span>
<span data-ttu-id="2fdff-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fdff-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fdff-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fdff-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fdff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdff-122">CommonParameters</span></span>
<span data-ttu-id="2fdff-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fdff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdff-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fdff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdff-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fdff-125">INPUTS</span></span>

### <span data-ttu-id="2fdff-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2fdff-126">None</span></span>

## <span data-ttu-id="2fdff-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fdff-127">OUTPUTS</span></span>

### <span data-ttu-id="2fdff-128">System. void</span><span class="sxs-lookup"><span data-stu-id="2fdff-128">System.Void</span></span>

## <span data-ttu-id="2fdff-129">Note</span><span class="sxs-lookup"><span data-stu-id="2fdff-129">NOTES</span></span>
<span data-ttu-id="2fdff-130">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="2fdff-130">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="2fdff-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fdff-131">RELATED LINKS</span></span>
