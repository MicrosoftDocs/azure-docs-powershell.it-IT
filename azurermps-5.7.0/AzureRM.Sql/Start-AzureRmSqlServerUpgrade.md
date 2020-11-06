---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d33635cd3876a3426c3db96489d623d0a61f1d03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519345"
---
# <span data-ttu-id="a1520-101">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="a1520-101">Start-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="a1520-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1520-102">SYNOPSIS</span></span>
<span data-ttu-id="a1520-103">Avvia l'aggiornamento di un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="a1520-103">Starts the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1520-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1520-104">SYNTAX</span></span>

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1520-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1520-105">DESCRIPTION</span></span>
<span data-ttu-id="a1520-106">Il cmdlet **Start-AzureRmSqlServerUpgrade** avvia l'aggiornamento di un server di database SQL di Azure versione 11 alla versione 12.</span><span class="sxs-lookup"><span data-stu-id="a1520-106">The **Start-AzureRmSqlServerUpgrade** cmdlet starts the upgrade of an Azure SQL Database server version 11 to version 12.</span></span>
<span data-ttu-id="a1520-107">È possibile monitorare lo stato di avanzamento di un aggiornamento usando il cmdlet Get-AzureRmSqlServerUpgrade.</span><span class="sxs-lookup"><span data-stu-id="a1520-107">You can monitor the progress of an upgrade by using the Get-AzureRmSqlServerUpgrade cmdlet.</span></span>

## <span data-ttu-id="a1520-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1520-108">EXAMPLES</span></span>

### <span data-ttu-id="a1520-109">Esempio 1: aggiornare un server</span><span class="sxs-lookup"><span data-stu-id="a1520-109">Example 1: Upgrade a server</span></span>
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

<span data-ttu-id="a1520-110">Questo comando consente di aggiornare il server denominato Server01 assegnato al gruppo di risorse TesourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a1520-110">This command upgrades the server named server01 assigned to resource group TesourceGroup01.</span></span>

### <span data-ttu-id="a1520-111">Esempio 2: aggiornare un server usando le indicazioni per orari e database</span><span class="sxs-lookup"><span data-stu-id="a1520-111">Example 2: Upgrade a server by using schedule time and database recommendation</span></span>
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

<span data-ttu-id="a1520-112">Il primo comando crea un tempo di cinque minuti in futuro usando il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="a1520-112">The first command creates a time five minutes in the future by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="a1520-113">Il comando Archivia la data nella variabile $ScheduleTime.</span><span class="sxs-lookup"><span data-stu-id="a1520-113">The command stores the date in the variable $ScheduleTime.</span></span>
<span data-ttu-id="a1520-114">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a1520-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="a1520-115">Il secondo comando crea un oggetto **RecommendedDatabaseProperties** e quindi archivia l'oggetto nella variabile $DatabaseMap.</span><span class="sxs-lookup"><span data-stu-id="a1520-115">The second command creates a **RecommendedDatabaseProperties** object, and then stores that object in the variable $DatabaseMap.</span></span>

<span data-ttu-id="a1520-116">I tre comandi seguenti assegnano i valori alle proprietà dell'oggetto archiviato in $DatabaseMap.</span><span class="sxs-lookup"><span data-stu-id="a1520-116">The next three commands assign values to properties of the object stored in $DatabaseMap.</span></span>

<span data-ttu-id="a1520-117">Il comando finale consente di aggiornare il server esistente denominato Server01 alla versione 12,0.</span><span class="sxs-lookup"><span data-stu-id="a1520-117">The final command upgrades the existing server named Server01 to version 12.0.</span></span>
<span data-ttu-id="a1520-118">Il momento più recente per l'aggiornamento è di cinque minuti dopo l'esecuzione del comando, come specificato dalla variabile $ScheduleTime.</span><span class="sxs-lookup"><span data-stu-id="a1520-118">The earliest time to upgrade is five minutes after you run the command, as specified by the $ScheduleTime variable.</span></span>
<span data-ttu-id="a1520-119">Dopo l'aggiornamento, il database ContosoDB eseguirà l'edizione standard e avrà l'obiettivo di livello di servizio S0.</span><span class="sxs-lookup"><span data-stu-id="a1520-119">After the upgrade, the database contosodb will be running the Standard edition and have the Service Level Objective S0.</span></span>

## <span data-ttu-id="a1520-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1520-120">PARAMETERS</span></span>

### <span data-ttu-id="a1520-121">-DatabaseCollection</span><span class="sxs-lookup"><span data-stu-id="a1520-121">-DatabaseCollection</span></span>
<span data-ttu-id="a1520-122">Specifica una matrice di oggetti **RecommendedDatabaseProperties** che questo cmdlet USA per l'aggiornamento del server.</span><span class="sxs-lookup"><span data-stu-id="a1520-122">Specifies an array of **RecommendedDatabaseProperties** objects that this cmdlet uses for the server upgrade.</span></span>

```yaml
Type: RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1520-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1520-123">-DefaultProfile</span></span>
<span data-ttu-id="a1520-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a1520-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1520-125">-ElasticPoolCollection</span><span class="sxs-lookup"><span data-stu-id="a1520-125">-ElasticPoolCollection</span></span>
<span data-ttu-id="a1520-126">Specifica una matrice di oggetti **UpgradeRecommendedElasticPoolProperties** da usare per l'aggiornamento del server.</span><span class="sxs-lookup"><span data-stu-id="a1520-126">Specifies an array of **UpgradeRecommendedElasticPoolProperties** objects to use for the server upgrade.</span></span>

```yaml
Type: UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1520-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1520-127">-ResourceGroupName</span></span>
<span data-ttu-id="a1520-128">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="a1520-128">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1520-129">-ScheduleUpgradeAfterUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="a1520-129">-ScheduleUpgradeAfterUtcDateTime</span></span>
<span data-ttu-id="a1520-130">Specifica il tempo più iniziale, come oggetto **DateTime** , per aggiornare il server.</span><span class="sxs-lookup"><span data-stu-id="a1520-130">Specifies the earliest time, as a **DateTime** object, to upgrade the server.</span></span>
<span data-ttu-id="a1520-131">Specificare un valore nel formato ISO8601, in ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="a1520-131">Specify a value in the ISO8601 format, in Coordinated Universal Time (UTC).</span></span>
<span data-ttu-id="a1520-132">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a1520-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1520-133">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a1520-133">-ServerName</span></span>
<span data-ttu-id="a1520-134">Specifica il nome del server che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="a1520-134">Specifies the name of the server that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1520-135">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="a1520-135">-ServerVersion</span></span>
<span data-ttu-id="a1520-136">Specifica la versione a cui questo cmdlet aggiorna il server.</span><span class="sxs-lookup"><span data-stu-id="a1520-136">Specifies the version to which this cmdlet upgrades the server.</span></span>
<span data-ttu-id="a1520-137">L'unico valore valido è 12,0.</span><span class="sxs-lookup"><span data-stu-id="a1520-137">The only valid value is 12.0.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1520-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1520-138">CommonParameters</span></span>
<span data-ttu-id="a1520-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1520-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1520-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1520-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1520-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1520-141">INPUTS</span></span>

### <span data-ttu-id="a1520-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a1520-142">None</span></span>
<span data-ttu-id="a1520-143">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a1520-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1520-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1520-144">OUTPUTS</span></span>

### <span data-ttu-id="a1520-145">Microsoft. Azure. Commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="a1520-145">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="a1520-146">Note</span><span class="sxs-lookup"><span data-stu-id="a1520-146">NOTES</span></span>

## <span data-ttu-id="a1520-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1520-147">RELATED LINKS</span></span>

[<span data-ttu-id="a1520-148">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="a1520-148">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="a1520-149">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="a1520-149">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="a1520-150">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="a1520-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


