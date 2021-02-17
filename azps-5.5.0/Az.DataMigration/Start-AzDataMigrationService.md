---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198094"
---
# <span data-ttu-id="06da4-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="06da4-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="06da4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06da4-102">SYNOPSIS</span></span>
<span data-ttu-id="06da4-103">Avvia un'istanza del servizio di migrazione dei database di Azure in uno stato di interruzione.</span><span class="sxs-lookup"><span data-stu-id="06da4-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="06da4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06da4-104">SYNTAX</span></span>

### <span data-ttu-id="06da4-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06da4-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06da4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06da4-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06da4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06da4-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06da4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="06da4-108">DESCRIPTION</span></span>
<span data-ttu-id="06da4-109">Il Start-AzDataMigrationService cmdlet avvia un'istanza del servizio di migrazione del database di Azure in uno stato di interruzione.</span><span class="sxs-lookup"><span data-stu-id="06da4-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="06da4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06da4-110">EXAMPLES</span></span>

### <span data-ttu-id="06da4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06da4-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="06da4-112">L'esempio precedente avvia un'istanza del servizio di migrazione del database di Azure denominata Servizio di test in stato di interruzione in base al nome del servizio passato come input</span><span class="sxs-lookup"><span data-stu-id="06da4-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="06da4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="06da4-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="06da4-114">L'esempio precedente avvia un'istanza del servizio di migrazione del database di Azure basata su PSDataMigrationService passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="06da4-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="06da4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06da4-115">PARAMETERS</span></span>

### <span data-ttu-id="06da4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06da4-116">-DefaultProfile</span></span>
<span data-ttu-id="06da4-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06da4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06da4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06da4-118">-InputObject</span></span>
<span data-ttu-id="06da4-119">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="06da4-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06da4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="06da4-120">-Name</span></span>
<span data-ttu-id="06da4-121">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="06da4-121">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06da4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06da4-122">-PassThru</span></span>
<span data-ttu-id="06da4-123">Restituisce vero/falso.</span><span class="sxs-lookup"><span data-stu-id="06da4-123">Returns an true/false.</span></span>
<span data-ttu-id="06da4-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="06da4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06da4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06da4-125">-ResourceGroupName</span></span>
<span data-ttu-id="06da4-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06da4-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06da4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06da4-127">-ResourceId</span></span>
<span data-ttu-id="06da4-128">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="06da4-128">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06da4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06da4-129">-Confirm</span></span>
<span data-ttu-id="06da4-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06da4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06da4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06da4-131">-WhatIf</span></span>
<span data-ttu-id="06da4-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06da4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06da4-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06da4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06da4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06da4-134">CommonParameters</span></span>
<span data-ttu-id="06da4-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06da4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06da4-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06da4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06da4-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="06da4-137">INPUTS</span></span>

### <span data-ttu-id="06da4-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="06da4-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="06da4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="06da4-139">System.String</span></span>

## <span data-ttu-id="06da4-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06da4-140">OUTPUTS</span></span>

### <span data-ttu-id="06da4-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06da4-141">System.Boolean</span></span>

## <span data-ttu-id="06da4-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="06da4-142">NOTES</span></span>

## <span data-ttu-id="06da4-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06da4-143">RELATED LINKS</span></span>
