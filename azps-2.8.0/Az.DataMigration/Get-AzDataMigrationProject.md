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
ms.locfileid: "93674744"
---
# <span data-ttu-id="e5c5a-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="e5c5a-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="e5c5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c5a-103">Recupera le proprietà di un progetto di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c5a-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="e5c5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5c5a-104">SYNTAX</span></span>

### <span data-ttu-id="e5c5a-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5c5a-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c5a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5c5a-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c5a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5c5a-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5c5a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5c5a-108">DESCRIPTION</span></span>
<span data-ttu-id="e5c5a-109">Il cmdlet Get-AzDataMigrationProject recupera le proprietà di un progetto di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c5a-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="e5c5a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5c5a-110">EXAMPLES</span></span>

### <span data-ttu-id="e5c5a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e5c5a-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="e5c5a-112">L'esempio precedente recupera il progetto di migrazione di database di Azure denominato TestProject nel gruppo di risorse denominato testResourceGroup e in servizio denominato testService</span><span class="sxs-lookup"><span data-stu-id="e5c5a-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="e5c5a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e5c5a-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="e5c5a-114">L'esempio precedente recupera il progetto di migrazione del database di Azure basato sul parametro di input dell'oggetto PSProject passato.</span><span class="sxs-lookup"><span data-stu-id="e5c5a-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="e5c5a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5c5a-115">PARAMETERS</span></span>

### <span data-ttu-id="e5c5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c5a-116">-DefaultProfile</span></span>
<span data-ttu-id="e5c5a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c5a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5c5a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5c5a-118">-InputObject</span></span>
<span data-ttu-id="e5c5a-119">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="e5c5a-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="e5c5a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5c5a-120">-Name</span></span>
<span data-ttu-id="e5c5a-121">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="e5c5a-121">The name of the project.</span></span>

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

### <span data-ttu-id="e5c5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="e5c5a-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5c5a-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="e5c5a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c5a-124">-ResourceId</span></span>
<span data-ttu-id="e5c5a-125">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="e5c5a-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="e5c5a-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e5c5a-126">-ServiceName</span></span>
<span data-ttu-id="e5c5a-127">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="e5c5a-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="e5c5a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c5a-128">CommonParameters</span></span>
<span data-ttu-id="e5c5a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c5a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c5a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c5a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c5a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5c5a-131">INPUTS</span></span>

### <span data-ttu-id="e5c5a-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e5c5a-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="e5c5a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e5c5a-133">System.String</span></span>

## <span data-ttu-id="e5c5a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5c5a-134">OUTPUTS</span></span>

### <span data-ttu-id="e5c5a-135">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="e5c5a-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="e5c5a-136">Note</span><span class="sxs-lookup"><span data-stu-id="e5c5a-136">NOTES</span></span>

## <span data-ttu-id="e5c5a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5c5a-137">RELATED LINKS</span></span>
