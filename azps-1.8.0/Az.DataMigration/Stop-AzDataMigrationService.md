---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: b838cef6b72c783c8a9252df1e448e27bd100e36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684478"
---
# <span data-ttu-id="818df-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="818df-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="818df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="818df-102">SYNOPSIS</span></span>
<span data-ttu-id="818df-103">Interrompe un'istanza del servizio di migrazione del database di Azure in uno stato in corso.</span><span class="sxs-lookup"><span data-stu-id="818df-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="818df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="818df-104">SYNTAX</span></span>

### <span data-ttu-id="818df-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="818df-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="818df-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="818df-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="818df-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="818df-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="818df-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="818df-108">DESCRIPTION</span></span>
<span data-ttu-id="818df-109">Il cmdlet Stop-AzDataMigrationService interrompe un'istanza del servizio di migrazione del database di Azure in uno stato in corso.</span><span class="sxs-lookup"><span data-stu-id="818df-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="818df-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="818df-110">EXAMPLES</span></span>

### <span data-ttu-id="818df-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="818df-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="818df-112">Nell'esempio precedente viene arrestata un'istanza del servizio di migrazione del database di Azure denominata TestService in base al nome del servizio passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="818df-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="818df-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="818df-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="818df-114">L'esempio precedente interrompe un'istanza del servizio di migrazione del database di Azure basato sull'oggetto PSDataMigrationService passato come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="818df-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="818df-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="818df-115">PARAMETERS</span></span>

### <span data-ttu-id="818df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="818df-116">-DefaultProfile</span></span>
<span data-ttu-id="818df-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="818df-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="818df-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="818df-118">-InputObject</span></span>
<span data-ttu-id="818df-119">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="818df-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="818df-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="818df-120">-Name</span></span>
<span data-ttu-id="818df-121">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="818df-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="818df-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="818df-122">-PassThru</span></span>
<span data-ttu-id="818df-123">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="818df-123">Returns an true/false.</span></span>
<span data-ttu-id="818df-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="818df-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="818df-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="818df-125">-ResourceGroupName</span></span>
<span data-ttu-id="818df-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="818df-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="818df-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="818df-127">-ResourceId</span></span>
<span data-ttu-id="818df-128">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="818df-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="818df-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="818df-129">-Confirm</span></span>
<span data-ttu-id="818df-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="818df-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="818df-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="818df-131">-WhatIf</span></span>
<span data-ttu-id="818df-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="818df-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="818df-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="818df-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="818df-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="818df-134">CommonParameters</span></span>
<span data-ttu-id="818df-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="818df-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="818df-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="818df-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="818df-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="818df-137">INPUTS</span></span>

### <span data-ttu-id="818df-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="818df-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="818df-139">System. String</span><span class="sxs-lookup"><span data-stu-id="818df-139">System.String</span></span>

## <span data-ttu-id="818df-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="818df-140">OUTPUTS</span></span>

### <span data-ttu-id="818df-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="818df-141">System.Boolean</span></span>

## <span data-ttu-id="818df-142">Note</span><span class="sxs-lookup"><span data-stu-id="818df-142">NOTES</span></span>

## <span data-ttu-id="818df-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="818df-143">RELATED LINKS</span></span>