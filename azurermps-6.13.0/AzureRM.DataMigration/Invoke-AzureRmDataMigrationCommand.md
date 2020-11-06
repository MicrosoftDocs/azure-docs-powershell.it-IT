---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Invoke-AzureRmDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
ms.openlocfilehash: 882d7eb0b005478850addda2d066c7266e6c2ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518695"
---
# <span data-ttu-id="cf52e-101">Invoke-AzureRmDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="cf52e-101">Invoke-AzureRmDataMigrationCommand</span></span>

## <span data-ttu-id="cf52e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf52e-102">SYNOPSIS</span></span>
<span data-ttu-id="cf52e-103">Crea un nuovo comando da eseguire in un'attività DMS esistente.</span><span class="sxs-lookup"><span data-stu-id="cf52e-103">Creates a new command to be executed on an existing DMS task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf52e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf52e-104">SYNTAX</span></span>

```
Invoke-AzureRmDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf52e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf52e-105">DESCRIPTION</span></span>
<span data-ttu-id="cf52e-106">Il cmdlet New-AzureRmDataMigrationCommand crea una nuova attività di comando da eseguire in un'attività di migrazione esistente.</span><span class="sxs-lookup"><span data-stu-id="cf52e-106">The New-AzureRmDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="cf52e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf52e-107">EXAMPLES</span></span>

### <span data-ttu-id="cf52e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cf52e-108">Example 1</span></span>
```
PS C:\> $command = New-AzureRmDmsCommand -CommandType Complete -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="cf52e-109">Gli esempi precedenti usano il cmdlet New-AzureRmDmsCommand per creare un comando per un servizio, un progetto e un'attività esistenti</span><span class="sxs-lookup"><span data-stu-id="cf52e-109">The above examples uses the New-AzureRmDmsCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="cf52e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf52e-110">PARAMETERS</span></span>

### <span data-ttu-id="cf52e-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="cf52e-111">-CommandType</span></span>
<span data-ttu-id="cf52e-112">Tipo di comando.</span><span class="sxs-lookup"><span data-stu-id="cf52e-112">Command Type.</span></span>

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

### <span data-ttu-id="cf52e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf52e-113">-DefaultProfile</span></span>
<span data-ttu-id="cf52e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf52e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf52e-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="cf52e-115">-ProjectName</span></span>
<span data-ttu-id="cf52e-116">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="cf52e-116">The name of the project.</span></span>

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

### <span data-ttu-id="cf52e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf52e-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf52e-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf52e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cf52e-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cf52e-119">-ServiceName</span></span>
<span data-ttu-id="cf52e-120">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="cf52e-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="cf52e-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="cf52e-121">-TaskName</span></span>
<span data-ttu-id="cf52e-122">Nome dell'attività in cui viene eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="cf52e-122">The name of the task the command is run on.</span></span>

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

### <span data-ttu-id="cf52e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf52e-123">-Confirm</span></span>
<span data-ttu-id="cf52e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf52e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf52e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf52e-125">-WhatIf</span></span>
<span data-ttu-id="cf52e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf52e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf52e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf52e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf52e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf52e-128">CommonParameters</span></span>
<span data-ttu-id="cf52e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf52e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf52e-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf52e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf52e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf52e-131">INPUTS</span></span>

### <span data-ttu-id="cf52e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cf52e-132">System.String</span></span>

## <span data-ttu-id="cf52e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf52e-133">OUTPUTS</span></span>

### <span data-ttu-id="cf52e-134">Microsoft. Azure. Management. DataMigration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="cf52e-134">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="cf52e-135">Note</span><span class="sxs-lookup"><span data-stu-id="cf52e-135">NOTES</span></span>

## <span data-ttu-id="cf52e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf52e-136">RELATED LINKS</span></span>
