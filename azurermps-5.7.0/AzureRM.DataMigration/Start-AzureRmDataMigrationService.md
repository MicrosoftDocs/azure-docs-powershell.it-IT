---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/start-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: 03f07eaac1dbf616c78d1ca39561945b2a844b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508171"
---
# <span data-ttu-id="42725-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="42725-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="42725-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42725-102">SYNOPSIS</span></span>
<span data-ttu-id="42725-103">Avvia un'istanza del servizio di migrazione del database di Azure in uno stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="42725-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42725-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42725-104">SYNTAX</span></span>

### <span data-ttu-id="42725-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42725-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="42725-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42725-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="42725-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42725-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="42725-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42725-108">DESCRIPTION</span></span>
<span data-ttu-id="42725-109">Il cmdlet Start-AzureRmDataMigrationService avvia un'istanza del servizio di migrazione del database di Azure in uno stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="42725-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="42725-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42725-110">EXAMPLES</span></span>

### <span data-ttu-id="42725-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="42725-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="42725-112">Nell'esempio precedente viene avviata un'istanza del servizio di migrazione del database di Azure denominata test service in uno stato interrotto in base al nome del servizio passato come input</span><span class="sxs-lookup"><span data-stu-id="42725-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="42725-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="42725-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="42725-114">L'esempio precedente avvia un'istanza del servizio di migrazione di database di Azure basata su PSDataMigrationService passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="42725-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="42725-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42725-115">PARAMETERS</span></span>

### <span data-ttu-id="42725-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="42725-116">-Confirm</span></span>
<span data-ttu-id="42725-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42725-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42725-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42725-118">-DefaultProfile</span></span>
<span data-ttu-id="42725-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42725-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42725-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42725-120">-InputObject</span></span>
<span data-ttu-id="42725-121">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="42725-121">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42725-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="42725-122">-Name</span></span>
<span data-ttu-id="42725-123">Nome del servizio di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="42725-123">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42725-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42725-124">-PassThru</span></span>
<span data-ttu-id="42725-125">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="42725-125">Returns an true/false.</span></span>
<span data-ttu-id="42725-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="42725-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42725-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42725-127">-ResourceGroupName</span></span>
<span data-ttu-id="42725-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42725-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42725-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42725-129">-ResourceId</span></span>
<span data-ttu-id="42725-130">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="42725-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42725-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42725-131">-WhatIf</span></span>
<span data-ttu-id="42725-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42725-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42725-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42725-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="42725-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42725-134">INPUTS</span></span>

### <span data-ttu-id="42725-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="42725-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="42725-136">System. String</span><span class="sxs-lookup"><span data-stu-id="42725-136">System.String</span></span>


## <span data-ttu-id="42725-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42725-137">OUTPUTS</span></span>

### <span data-ttu-id="42725-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42725-138">System.Boolean</span></span>


## <span data-ttu-id="42725-139">Note</span><span class="sxs-lookup"><span data-stu-id="42725-139">NOTES</span></span>

## <span data-ttu-id="42725-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42725-140">RELATED LINKS</span></span>


