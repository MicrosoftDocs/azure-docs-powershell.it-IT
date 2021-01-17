---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473527"
---
# <span data-ttu-id="5e7be-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="5e7be-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="5e7be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e7be-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7be-103">Recupera le proprietà di un progetto di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e7be-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="5e7be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e7be-104">SYNTAX</span></span>

### <span data-ttu-id="5e7be-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e7be-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e7be-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e7be-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e7be-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e7be-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e7be-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e7be-108">DESCRIPTION</span></span>
<span data-ttu-id="5e7be-109">Il cmdlet Get-AzDataMigrationProject recupera le proprietà di un progetto di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e7be-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="5e7be-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e7be-110">EXAMPLES</span></span>

### <span data-ttu-id="5e7be-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5e7be-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="5e7be-112">L'esempio precedente recupera il progetto di migrazione di database di Azure denominato TestProject nel gruppo di risorse denominato testResourceGroup e in servizio denominato testService</span><span class="sxs-lookup"><span data-stu-id="5e7be-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="5e7be-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5e7be-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="5e7be-114">L'esempio precedente recupera il progetto di migrazione del database di Azure basato sul parametro di input dell'oggetto PSProject passato.</span><span class="sxs-lookup"><span data-stu-id="5e7be-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="5e7be-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e7be-115">PARAMETERS</span></span>

### <span data-ttu-id="5e7be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e7be-116">-DefaultProfile</span></span>
<span data-ttu-id="5e7be-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e7be-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e7be-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e7be-118">-InputObject</span></span>
<span data-ttu-id="5e7be-119">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="5e7be-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="5e7be-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e7be-120">-Name</span></span>
<span data-ttu-id="5e7be-121">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="5e7be-121">The name of the project.</span></span>

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

### <span data-ttu-id="5e7be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e7be-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e7be-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e7be-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e7be-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e7be-124">-ResourceId</span></span>
<span data-ttu-id="5e7be-125">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="5e7be-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="5e7be-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5e7be-126">-ServiceName</span></span>
<span data-ttu-id="5e7be-127">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="5e7be-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="5e7be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7be-128">CommonParameters</span></span>
<span data-ttu-id="5e7be-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e7be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7be-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e7be-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7be-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e7be-131">INPUTS</span></span>

### <span data-ttu-id="5e7be-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5e7be-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="5e7be-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5e7be-133">System.String</span></span>

## <span data-ttu-id="5e7be-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e7be-134">OUTPUTS</span></span>

### <span data-ttu-id="5e7be-135">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="5e7be-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="5e7be-136">Note</span><span class="sxs-lookup"><span data-stu-id="5e7be-136">NOTES</span></span>

## <span data-ttu-id="5e7be-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e7be-137">RELATED LINKS</span></span>
