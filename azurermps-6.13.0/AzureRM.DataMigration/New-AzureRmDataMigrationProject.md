---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 9abb97e5006f6572c7a0b08d8d25bcc55906a765
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515376"
---
# <span data-ttu-id="26e80-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="26e80-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="26e80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26e80-102">SYNOPSIS</span></span>
<span data-ttu-id="26e80-103">Crea un nuovo progetto di servizio di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="26e80-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26e80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26e80-104">SYNTAX</span></span>

### <span data-ttu-id="26e80-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26e80-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e80-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e80-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e80-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e80-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26e80-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26e80-108">DESCRIPTION</span></span>
<span data-ttu-id="26e80-109">Il cmdlet New-AzureRmDataMigrationProject crea un nuovo progetto di servizio di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="26e80-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="26e80-110">Questo cmdlet accetta tutti i parametri necessari, ad esempio il nome del gruppo di risorse di Azure, il nome del servizio di migrazione dei dati di Azure in cui deve essere creato il nuovo progetto, l'area geografica in cui deve essere creato il progetto, il nome univoco del nuovo progetto, gli oggetti di connessione di origine e di destinazione e l'oggetto tipo di destinazione, come input per l'elenco di database</span><span class="sxs-lookup"><span data-stu-id="26e80-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="26e80-111">Usa il cmdlet New-AzureRmDataMigrationConnectionInfo per creare un nuovo oggetto ConnectionInfo per le connessioni di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="26e80-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="26e80-112">L'elenco di Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo è previsto per i database selezionati. Questo oggetto può essere creato usando il cmdlet New-AzureRmDataMigrationDatabaseInfo.</span><span class="sxs-lookup"><span data-stu-id="26e80-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="26e80-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26e80-113">EXAMPLES</span></span>

### <span data-ttu-id="26e80-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26e80-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="26e80-115">Nell'esempio precedente viene illustrato come creare un nuovo progetto denominato MyDMSProject situato nell'area centrale degli Stati Uniti nell'istanza del servizio di migrazione del database di Azure denominata TestService.</span><span class="sxs-lookup"><span data-stu-id="26e80-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="26e80-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26e80-116">PARAMETERS</span></span>

### <span data-ttu-id="26e80-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="26e80-117">-DatabaseInfo</span></span>
<span data-ttu-id="26e80-118">Informazioni sul database.</span><span class="sxs-lookup"><span data-stu-id="26e80-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e80-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e80-119">-DefaultProfile</span></span>
<span data-ttu-id="26e80-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26e80-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e80-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26e80-121">-InputObject</span></span>
<span data-ttu-id="26e80-122">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="26e80-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="26e80-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="26e80-123">-Location</span></span>
<span data-ttu-id="26e80-124">Posizione dell'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="26e80-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e80-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="26e80-125">-Name</span></span>
<span data-ttu-id="26e80-126">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="26e80-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e80-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e80-127">-ResourceGroupName</span></span>
<span data-ttu-id="26e80-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26e80-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="26e80-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e80-129">-ResourceId</span></span>
<span data-ttu-id="26e80-130">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="26e80-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="26e80-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="26e80-131">-ServiceName</span></span>
<span data-ttu-id="26e80-132">Nome dell'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="26e80-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="26e80-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="26e80-133">-SourceConnection</span></span>
<span data-ttu-id="26e80-134">Informazioni sulla connessione di origine.</span><span class="sxs-lookup"><span data-stu-id="26e80-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e80-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="26e80-135">-SourceType</span></span>
<span data-ttu-id="26e80-136">Tipo di piattaforma di origine per Project.</span><span class="sxs-lookup"><span data-stu-id="26e80-136">Source platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e80-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="26e80-137">-TargetConnection</span></span>
<span data-ttu-id="26e80-138">Informazioni sulla connessione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="26e80-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e80-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="26e80-139">-TargetType</span></span>
<span data-ttu-id="26e80-140">Tipo di piattaforma di destinazione per Project.</span><span class="sxs-lookup"><span data-stu-id="26e80-140">Target platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e80-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26e80-141">-Confirm</span></span>
<span data-ttu-id="26e80-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e80-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e80-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e80-143">-WhatIf</span></span>
<span data-ttu-id="26e80-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26e80-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26e80-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26e80-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e80-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e80-146">CommonParameters</span></span>
<span data-ttu-id="26e80-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e80-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e80-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e80-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e80-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26e80-149">INPUTS</span></span>

### <span data-ttu-id="26e80-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="26e80-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="26e80-151">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="26e80-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="26e80-152">System. String</span><span class="sxs-lookup"><span data-stu-id="26e80-152">System.String</span></span>

## <span data-ttu-id="26e80-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26e80-153">OUTPUTS</span></span>

### <span data-ttu-id="26e80-154">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="26e80-154">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="26e80-155">Note</span><span class="sxs-lookup"><span data-stu-id="26e80-155">NOTES</span></span>

## <span data-ttu-id="26e80-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26e80-156">RELATED LINKS</span></span>
