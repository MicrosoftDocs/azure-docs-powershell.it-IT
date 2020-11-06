---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 9a3028e019d3873105df079b67652f2157137ce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521925"
---
# <span data-ttu-id="29528-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="29528-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="29528-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29528-102">SYNOPSIS</span></span>
<span data-ttu-id="29528-103">Interrompe un'istanza del servizio di migrazione del database di Azure in uno stato in corso.</span><span class="sxs-lookup"><span data-stu-id="29528-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29528-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29528-104">SYNTAX</span></span>

### <span data-ttu-id="29528-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29528-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="29528-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29528-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="29528-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29528-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="29528-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29528-108">DESCRIPTION</span></span>
<span data-ttu-id="29528-109">Il cmdlet Stop-AzureRmDataMigrationService interrompe un'istanza del servizio di migrazione del database di Azure in uno stato in corso.</span><span class="sxs-lookup"><span data-stu-id="29528-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="29528-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29528-110">EXAMPLES</span></span>

### <span data-ttu-id="29528-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="29528-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService

```
<span data-ttu-id="29528-112">Nell'esempio precedente viene arrestata un'istanza del servizio di migrazione del database di Azure denominata TestService in base al nome del servizio passato come parametro di input</span><span class="sxs-lookup"><span data-stu-id="29528-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="29528-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="29528-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService

```
<span data-ttu-id="29528-114">L'esempio precedente interrompe un'istanza del servizio di migrazione del database di Azure basato sull'oggetto PSDataMigrationService passato come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="29528-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>



## <span data-ttu-id="29528-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29528-115">PARAMETERS</span></span>

### <span data-ttu-id="29528-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="29528-116">-Confirm</span></span>
<span data-ttu-id="29528-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29528-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29528-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29528-118">-DefaultProfile</span></span>
<span data-ttu-id="29528-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29528-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29528-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29528-120">-InputObject</span></span>
<span data-ttu-id="29528-121">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="29528-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="29528-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="29528-122">-Name</span></span>
<span data-ttu-id="29528-123">Nome del servizio di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="29528-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="29528-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29528-124">-PassThru</span></span>
<span data-ttu-id="29528-125">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="29528-125">Returns an true/false.</span></span>
<span data-ttu-id="29528-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="29528-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29528-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29528-127">-ResourceGroupName</span></span>
<span data-ttu-id="29528-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="29528-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="29528-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29528-129">-ResourceId</span></span>
<span data-ttu-id="29528-130">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="29528-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="29528-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29528-131">-WhatIf</span></span>
<span data-ttu-id="29528-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="29528-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29528-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="29528-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="29528-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29528-134">INPUTS</span></span>

### <span data-ttu-id="29528-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="29528-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="29528-136">System. String</span><span class="sxs-lookup"><span data-stu-id="29528-136">System.String</span></span>


## <span data-ttu-id="29528-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29528-137">OUTPUTS</span></span>

### <span data-ttu-id="29528-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29528-138">System.Boolean</span></span>


## <span data-ttu-id="29528-139">Note</span><span class="sxs-lookup"><span data-stu-id="29528-139">NOTES</span></span>

## <span data-ttu-id="29528-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29528-140">RELATED LINKS</span></span>

