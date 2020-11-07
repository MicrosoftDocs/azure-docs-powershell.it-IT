---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 00a0e0a688f49615cadff3990071cd49d1356443
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684503"
---
# <span data-ttu-id="42e3e-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="42e3e-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="42e3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="42e3e-103">Recupera le proprietà di un progetto di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="42e3e-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="42e3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42e3e-104">SYNTAX</span></span>

### <span data-ttu-id="42e3e-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42e3e-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42e3e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42e3e-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42e3e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42e3e-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42e3e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42e3e-108">DESCRIPTION</span></span>
<span data-ttu-id="42e3e-109">Il cmdlet Get-AzDataMigrationProject recupera le proprietà di un progetto di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="42e3e-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="42e3e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42e3e-110">EXAMPLES</span></span>

### <span data-ttu-id="42e3e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="42e3e-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="42e3e-112">L'esempio precedente recupera il progetto di migrazione di database di Azure denominato TestProject nel gruppo di risorse denominato testResourceGroup e in servizio denominato testService</span><span class="sxs-lookup"><span data-stu-id="42e3e-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="42e3e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="42e3e-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="42e3e-114">L'esempio precedente recupera il progetto di migrazione del database di Azure basato sul parametro di input dell'oggetto PSProject passato.</span><span class="sxs-lookup"><span data-stu-id="42e3e-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="42e3e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42e3e-115">PARAMETERS</span></span>

### <span data-ttu-id="42e3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e3e-116">-DefaultProfile</span></span>
<span data-ttu-id="42e3e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42e3e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42e3e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42e3e-118">-InputObject</span></span>
<span data-ttu-id="42e3e-119">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="42e3e-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="42e3e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="42e3e-120">-Name</span></span>
<span data-ttu-id="42e3e-121">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="42e3e-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e3e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42e3e-122">-ResourceGroupName</span></span>
<span data-ttu-id="42e3e-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42e3e-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="42e3e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42e3e-124">-ResourceId</span></span>
<span data-ttu-id="42e3e-125">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="42e3e-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="42e3e-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="42e3e-126">-ServiceName</span></span>
<span data-ttu-id="42e3e-127">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="42e3e-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="42e3e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e3e-128">CommonParameters</span></span>
<span data-ttu-id="42e3e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e3e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e3e-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42e3e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e3e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42e3e-131">INPUTS</span></span>

### <span data-ttu-id="42e3e-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="42e3e-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="42e3e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="42e3e-133">System.String</span></span>

## <span data-ttu-id="42e3e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42e3e-134">OUTPUTS</span></span>

### <span data-ttu-id="42e3e-135">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="42e3e-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="42e3e-136">Note</span><span class="sxs-lookup"><span data-stu-id="42e3e-136">NOTES</span></span>

## <span data-ttu-id="42e3e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42e3e-137">RELATED LINKS</span></span>