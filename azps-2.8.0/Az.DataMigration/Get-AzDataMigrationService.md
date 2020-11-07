---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: dcb9d6e58a743f37aa71d91b0b73772c239f252e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674743"
---
# <span data-ttu-id="78c1f-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="78c1f-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="78c1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="78c1f-103">Recupera le proprietà associate a un'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="78c1f-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="78c1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78c1f-104">SYNTAX</span></span>

### <span data-ttu-id="78c1f-105">ResourceGroupSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78c1f-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78c1f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78c1f-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78c1f-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="78c1f-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78c1f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78c1f-108">DESCRIPTION</span></span>
<span data-ttu-id="78c1f-109">Il cmdlet Get-AzDataMigrationService recupera le proprietà associate a un'istanza del servizio di migrazione del database di Azure in base al nome del servizio e al nome del gruppo di risorse Azure come parametri di input.</span><span class="sxs-lookup"><span data-stu-id="78c1f-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="78c1f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78c1f-110">EXAMPLES</span></span>

### <span data-ttu-id="78c1f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="78c1f-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="78c1f-112">L'esempio precedente recupera le proprietà dell'istanza del servizio di migrazione del database di Azure denominata testService.</span><span class="sxs-lookup"><span data-stu-id="78c1f-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="78c1f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="78c1f-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="78c1f-114">L'esempio precedente recupera i servizi di migrazione di database di Azure nel gruppo risorse denominato testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="78c1f-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="78c1f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78c1f-115">PARAMETERS</span></span>

### <span data-ttu-id="78c1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c1f-116">-DefaultProfile</span></span>
<span data-ttu-id="78c1f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78c1f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78c1f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="78c1f-118">-Name</span></span>
<span data-ttu-id="78c1f-119">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="78c1f-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c1f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78c1f-120">-ResourceGroupName</span></span>
<span data-ttu-id="78c1f-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="78c1f-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c1f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78c1f-122">-ResourceId</span></span>
<span data-ttu-id="78c1f-123">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="78c1f-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="78c1f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c1f-124">CommonParameters</span></span>
<span data-ttu-id="78c1f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78c1f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c1f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c1f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c1f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78c1f-127">INPUTS</span></span>

### <span data-ttu-id="78c1f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="78c1f-128">System.String</span></span>

## <span data-ttu-id="78c1f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78c1f-129">OUTPUTS</span></span>

### <span data-ttu-id="78c1f-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="78c1f-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="78c1f-131">Note</span><span class="sxs-lookup"><span data-stu-id="78c1f-131">NOTES</span></span>

## <span data-ttu-id="78c1f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78c1f-132">RELATED LINKS</span></span>
