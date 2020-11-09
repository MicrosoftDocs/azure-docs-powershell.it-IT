---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297594"
---
# <span data-ttu-id="99ea8-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="99ea8-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="99ea8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="99ea8-103">Avvia un'istanza del servizio di migrazione del database di Azure in uno stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="99ea8-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="99ea8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99ea8-104">SYNTAX</span></span>

### <span data-ttu-id="99ea8-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99ea8-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99ea8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99ea8-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99ea8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99ea8-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99ea8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99ea8-108">DESCRIPTION</span></span>
<span data-ttu-id="99ea8-109">Il cmdlet Start-AzDataMigrationService avvia un'istanza del servizio di migrazione del database di Azure in uno stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="99ea8-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="99ea8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99ea8-110">EXAMPLES</span></span>

### <span data-ttu-id="99ea8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99ea8-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="99ea8-112">Nell'esempio precedente viene avviata un'istanza del servizio di migrazione del database di Azure denominata test service in uno stato interrotto in base al nome del servizio passato come input</span><span class="sxs-lookup"><span data-stu-id="99ea8-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="99ea8-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="99ea8-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="99ea8-114">L'esempio precedente avvia un'istanza del servizio di migrazione di database di Azure basata su PSDataMigrationService passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="99ea8-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="99ea8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99ea8-115">PARAMETERS</span></span>

### <span data-ttu-id="99ea8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ea8-116">-DefaultProfile</span></span>
<span data-ttu-id="99ea8-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99ea8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99ea8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99ea8-118">-InputObject</span></span>
<span data-ttu-id="99ea8-119">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="99ea8-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="99ea8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="99ea8-120">-Name</span></span>
<span data-ttu-id="99ea8-121">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="99ea8-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="99ea8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99ea8-122">-PassThru</span></span>
<span data-ttu-id="99ea8-123">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="99ea8-123">Returns an true/false.</span></span>
<span data-ttu-id="99ea8-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="99ea8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="99ea8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ea8-125">-ResourceGroupName</span></span>
<span data-ttu-id="99ea8-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99ea8-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="99ea8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99ea8-127">-ResourceId</span></span>
<span data-ttu-id="99ea8-128">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="99ea8-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="99ea8-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99ea8-129">-Confirm</span></span>
<span data-ttu-id="99ea8-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99ea8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99ea8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99ea8-131">-WhatIf</span></span>
<span data-ttu-id="99ea8-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99ea8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ea8-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99ea8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99ea8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ea8-134">CommonParameters</span></span>
<span data-ttu-id="99ea8-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ea8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ea8-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99ea8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ea8-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99ea8-137">INPUTS</span></span>

### <span data-ttu-id="99ea8-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="99ea8-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="99ea8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="99ea8-139">System.String</span></span>

## <span data-ttu-id="99ea8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99ea8-140">OUTPUTS</span></span>

### <span data-ttu-id="99ea8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99ea8-141">System.Boolean</span></span>

## <span data-ttu-id="99ea8-142">Note</span><span class="sxs-lookup"><span data-stu-id="99ea8-142">NOTES</span></span>

## <span data-ttu-id="99ea8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99ea8-143">RELATED LINKS</span></span>
