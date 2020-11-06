---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Start-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: a8440ddc7249068486f94c30e28e1b1be2e2413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521862"
---
# <span data-ttu-id="5adb3-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5adb3-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="5adb3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5adb3-102">SYNOPSIS</span></span>
<span data-ttu-id="5adb3-103">Avvia un'istanza del servizio di migrazione del database di Azure in uno stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="5adb3-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5adb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5adb3-104">SYNTAX</span></span>

### <span data-ttu-id="5adb3-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5adb3-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5adb3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5adb3-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5adb3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5adb3-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5adb3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5adb3-108">DESCRIPTION</span></span>
<span data-ttu-id="5adb3-109">Il cmdlet Start-AzureRmDataMigrationService avvia un'istanza del servizio di migrazione del database di Azure in uno stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="5adb3-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="5adb3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5adb3-110">EXAMPLES</span></span>

### <span data-ttu-id="5adb3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5adb3-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="5adb3-112">Nell'esempio precedente viene avviata un'istanza del servizio di migrazione del database di Azure denominata test service in uno stato interrotto in base al nome del servizio passato come input</span><span class="sxs-lookup"><span data-stu-id="5adb3-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="5adb3-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5adb3-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="5adb3-114">L'esempio precedente avvia un'istanza del servizio di migrazione di database di Azure basata su PSDataMigrationService passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="5adb3-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="5adb3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5adb3-115">PARAMETERS</span></span>

### <span data-ttu-id="5adb3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5adb3-116">-DefaultProfile</span></span>
<span data-ttu-id="5adb3-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5adb3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5adb3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5adb3-118">-InputObject</span></span>
<span data-ttu-id="5adb3-119">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="5adb3-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="5adb3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5adb3-120">-Name</span></span>
<span data-ttu-id="5adb3-121">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="5adb3-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="5adb3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5adb3-122">-PassThru</span></span>
<span data-ttu-id="5adb3-123">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="5adb3-123">Returns an true/false.</span></span>
<span data-ttu-id="5adb3-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="5adb3-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5adb3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5adb3-125">-ResourceGroupName</span></span>
<span data-ttu-id="5adb3-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5adb3-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="5adb3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5adb3-127">-ResourceId</span></span>
<span data-ttu-id="5adb3-128">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="5adb3-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="5adb3-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5adb3-129">-Confirm</span></span>
<span data-ttu-id="5adb3-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5adb3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5adb3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5adb3-131">-WhatIf</span></span>
<span data-ttu-id="5adb3-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5adb3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5adb3-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5adb3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5adb3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5adb3-134">CommonParameters</span></span>
<span data-ttu-id="5adb3-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5adb3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5adb3-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5adb3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5adb3-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5adb3-137">INPUTS</span></span>

### <span data-ttu-id="5adb3-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5adb3-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="5adb3-139">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5adb3-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5adb3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5adb3-140">System.String</span></span>

## <span data-ttu-id="5adb3-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5adb3-141">OUTPUTS</span></span>

### <span data-ttu-id="5adb3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5adb3-142">System.Boolean</span></span>

## <span data-ttu-id="5adb3-143">Note</span><span class="sxs-lookup"><span data-stu-id="5adb3-143">NOTES</span></span>

## <span data-ttu-id="5adb3-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5adb3-144">RELATED LINKS</span></span>
