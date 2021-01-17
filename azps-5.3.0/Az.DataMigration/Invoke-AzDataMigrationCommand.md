---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473524"
---
# <span data-ttu-id="2d54f-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="2d54f-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="2d54f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d54f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d54f-103">Crea un nuovo comando da eseguire in un'attività DMS esistente.</span><span class="sxs-lookup"><span data-stu-id="2d54f-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="2d54f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d54f-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="2d54f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d54f-105">DESCRIPTION</span></span>
<span data-ttu-id="2d54f-106">Il cmdlet Invoke-AzDataMigrationCommand crea una nuova attività di comando da eseguire in un'attività di migrazione esistente.</span><span class="sxs-lookup"><span data-stu-id="2d54f-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="2d54f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d54f-107">EXAMPLES</span></span>

### <span data-ttu-id="2d54f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2d54f-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="2d54f-109">Gli esempi precedenti usano il cmdlet Invoke-AzDataMigrationCommand per creare un comando per un servizio, un progetto e un'attività esistenti</span><span class="sxs-lookup"><span data-stu-id="2d54f-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="2d54f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d54f-110">PARAMETERS</span></span>

### <span data-ttu-id="2d54f-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="2d54f-111">-CommandType</span></span>
<span data-ttu-id="2d54f-112">Tipo di comando.</span><span class="sxs-lookup"><span data-stu-id="2d54f-112">Command Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.CommandTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: CompleteSqlDBSync, CancelMongoDB, RestartMongoDB, FinishMongoDB, CompleteSqlMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d54f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d54f-113">-DefaultProfile</span></span>
<span data-ttu-id="2d54f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d54f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d54f-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="2d54f-115">-ProjectName</span></span>
<span data-ttu-id="2d54f-116">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="2d54f-116">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d54f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d54f-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d54f-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2d54f-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d54f-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2d54f-119">-ServiceName</span></span>
<span data-ttu-id="2d54f-120">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="2d54f-120">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d54f-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="2d54f-121">-TaskName</span></span>
<span data-ttu-id="2d54f-122">Nome dell'attività in cui viene eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="2d54f-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="2d54f-123">-NomeOggetto</span><span class="sxs-lookup"><span data-stu-id="2d54f-123">-ObjectName</span></span>
<span data-ttu-id="2d54f-124">Nome dell'oggetto di database su cui verrà eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="2d54f-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="2d54f-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d54f-125">-Confirm</span></span>
<span data-ttu-id="2d54f-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d54f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d54f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d54f-127">-WhatIf</span></span>
<span data-ttu-id="2d54f-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d54f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d54f-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d54f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d54f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d54f-130">CommonParameters</span></span>
<span data-ttu-id="2d54f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d54f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d54f-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d54f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d54f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d54f-133">INPUTS</span></span>

### <span data-ttu-id="2d54f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2d54f-134">System.String</span></span>

## <span data-ttu-id="2d54f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d54f-135">OUTPUTS</span></span>

### <span data-ttu-id="2d54f-136">Microsoft. Azure. Management. DataMigration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="2d54f-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="2d54f-137">Note</span><span class="sxs-lookup"><span data-stu-id="2d54f-137">NOTES</span></span>

## <span data-ttu-id="2d54f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d54f-138">RELATED LINKS</span></span>
