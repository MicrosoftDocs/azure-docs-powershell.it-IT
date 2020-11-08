---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190252"
---
# <span data-ttu-id="3e9ea-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="3e9ea-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="3e9ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="3e9ea-103">Crea un nuovo comando da eseguire in un'attività DMS esistente.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="3e9ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e9ea-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="3e9ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e9ea-105">DESCRIPTION</span></span>
<span data-ttu-id="3e9ea-106">Il cmdlet Invoke-AzDataMigrationCommand crea una nuova attività di comando da eseguire in un'attività di migrazione esistente.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="3e9ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e9ea-107">EXAMPLES</span></span>

### <span data-ttu-id="3e9ea-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e9ea-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="3e9ea-109">Gli esempi precedenti usano il cmdlet Invoke-AzDataMigrationCommand per creare un comando per un servizio, un progetto e un'attività esistenti</span><span class="sxs-lookup"><span data-stu-id="3e9ea-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="3e9ea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e9ea-110">PARAMETERS</span></span>

### <span data-ttu-id="3e9ea-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="3e9ea-111">-CommandType</span></span>
<span data-ttu-id="3e9ea-112">Tipo di comando.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-112">Command Type.</span></span>

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

### <span data-ttu-id="3e9ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e9ea-113">-DefaultProfile</span></span>
<span data-ttu-id="3e9ea-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e9ea-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="3e9ea-115">-ProjectName</span></span>
<span data-ttu-id="3e9ea-116">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-116">The name of the project.</span></span>

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

### <span data-ttu-id="3e9ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e9ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e9ea-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="3e9ea-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3e9ea-119">-ServiceName</span></span>
<span data-ttu-id="3e9ea-120">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="3e9ea-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="3e9ea-121">-TaskName</span></span>
<span data-ttu-id="3e9ea-122">Nome dell'attività in cui viene eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="3e9ea-123">-NomeOggetto</span><span class="sxs-lookup"><span data-stu-id="3e9ea-123">-ObjectName</span></span>
<span data-ttu-id="3e9ea-124">Nome dell'oggetto di database su cui verrà eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="3e9ea-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e9ea-125">-Confirm</span></span>
<span data-ttu-id="3e9ea-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e9ea-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e9ea-127">-WhatIf</span></span>
<span data-ttu-id="3e9ea-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e9ea-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e9ea-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e9ea-130">CommonParameters</span></span>
<span data-ttu-id="3e9ea-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e9ea-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e9ea-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e9ea-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e9ea-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e9ea-133">INPUTS</span></span>

### <span data-ttu-id="3e9ea-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3e9ea-134">System.String</span></span>

## <span data-ttu-id="3e9ea-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e9ea-135">OUTPUTS</span></span>

### <span data-ttu-id="3e9ea-136">Microsoft. Azure. Management. DataMigration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="3e9ea-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="3e9ea-137">Note</span><span class="sxs-lookup"><span data-stu-id="3e9ea-137">NOTES</span></span>

## <span data-ttu-id="3e9ea-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e9ea-138">RELATED LINKS</span></span>