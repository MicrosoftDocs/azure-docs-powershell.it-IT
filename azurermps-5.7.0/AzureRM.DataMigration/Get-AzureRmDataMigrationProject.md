---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: ea6406d83004d9a7d21a2f47aba0c39a10caf59a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520467"
---
# <span data-ttu-id="bf550-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="bf550-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="bf550-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf550-102">SYNOPSIS</span></span>
<span data-ttu-id="bf550-103">Recupera le proprietà di un progetto di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf550-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf550-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf550-104">SYNTAX</span></span>

### <span data-ttu-id="bf550-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bf550-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="bf550-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf550-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="bf550-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf550-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="bf550-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf550-108">DESCRIPTION</span></span>
<span data-ttu-id="bf550-109">Il cmdlet Get-AzureRmDataMigrationProject recupera le proprietà di un progetto di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf550-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="bf550-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf550-110">EXAMPLES</span></span>

### <span data-ttu-id="bf550-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bf550-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="bf550-112">L'esempio precedente recupera il progetto di migrazione di database di Azure denominato TestProject nel gruppo di risorse denominato testResourceGroup e in servizio denominato testService</span><span class="sxs-lookup"><span data-stu-id="bf550-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="bf550-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bf550-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="bf550-114">L'esempio precedente recupera il progetto di migrazione del database di Azure basato sul parametro di input dell'oggetto PSProject passato.</span><span class="sxs-lookup"><span data-stu-id="bf550-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 


## <span data-ttu-id="bf550-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf550-115">PARAMETERS</span></span>

### <span data-ttu-id="bf550-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf550-116">-DefaultProfile</span></span>
<span data-ttu-id="bf550-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf550-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf550-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf550-118">-InputObject</span></span>
<span data-ttu-id="bf550-119">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="bf550-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="bf550-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf550-120">-Name</span></span>
<span data-ttu-id="bf550-121">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="bf550-121">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf550-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf550-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf550-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bf550-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="bf550-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf550-124">-ResourceId</span></span>
<span data-ttu-id="bf550-125">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="bf550-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="bf550-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bf550-126">-ServiceName</span></span>
<span data-ttu-id="bf550-127">Nome del servizio di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="bf550-127">Data Migration Service Name.</span></span>

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

## <span data-ttu-id="bf550-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf550-128">INPUTS</span></span>

### <span data-ttu-id="bf550-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="bf550-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="bf550-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bf550-130">System.String</span></span>


## <span data-ttu-id="bf550-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf550-131">OUTPUTS</span></span>

### <span data-ttu-id="bf550-132">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. DataMigration. Models. PSProject, Microsoft. Azure. Commands. DataMigration, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bf550-132">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProject, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="bf550-133">Note</span><span class="sxs-lookup"><span data-stu-id="bf550-133">NOTES</span></span>

## <span data-ttu-id="bf550-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf550-134">RELATED LINKS</span></span>

