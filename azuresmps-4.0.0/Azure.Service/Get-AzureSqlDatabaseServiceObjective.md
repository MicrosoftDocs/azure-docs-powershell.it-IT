---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023526"
---
# <span data-ttu-id="470b4-101">Get-AzureSqlDatabaseServiceObjective</span><span class="sxs-lookup"><span data-stu-id="470b4-101">Get-AzureSqlDatabaseServiceObjective</span></span>

## <span data-ttu-id="470b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="470b4-102">SYNOPSIS</span></span>
<span data-ttu-id="470b4-103">Ottiene gli obiettivi di servizio per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="470b4-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="470b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="470b4-104">SYNTAX</span></span>

### <span data-ttu-id="470b4-105">ByConnectionContext (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="470b4-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="470b4-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="470b4-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="470b4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="470b4-107">DESCRIPTION</span></span>
<span data-ttu-id="470b4-108">Il cmdlet **Get-AzureSqlDatabaseServiceObjective** ottiene gli obiettivi di servizio per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="470b4-108">The **Get-AzureSqlDatabaseServiceObjective** cmdlet gets service objectives for an Azure SQL Database server.</span></span>
<span data-ttu-id="470b4-109">Gli obiettivi di servizio sono definiti livelli di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="470b4-109">Service objectives are referred to as performance levels.</span></span>
<span data-ttu-id="470b4-110">Se non specifichi un obiettivo di servizio, questo cmdlet restituisce tutti gli obiettivi di servizio validi per il server specificato.</span><span class="sxs-lookup"><span data-stu-id="470b4-110">If you do not specify a service objective, this cmdlet returns all valid service objectives for the specified server.</span></span>

<span data-ttu-id="470b4-111">Questo cmdlet si applica ai livelli di servizio di base, standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="470b4-111">This cmdlet applies to Basic, Standard, and Premium service tiers.</span></span>

## <span data-ttu-id="470b4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="470b4-112">EXAMPLES</span></span>

### <span data-ttu-id="470b4-113">Esempio 1: ottenere tutti gli obiettivi del servizio usando un contesto di connessione</span><span class="sxs-lookup"><span data-stu-id="470b4-113">Example 1: Get all the service objectives by using a connection context</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

<span data-ttu-id="470b4-114">Questo comando ottiene tutti gli obiettivi di servizio per il server che il contesto di connessione $Context specifica.</span><span class="sxs-lookup"><span data-stu-id="470b4-114">This command gets all the service objectives for the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="470b4-115">Esempio 2: ottenere tutti gli obiettivi del servizio usando un nome di server</span><span class="sxs-lookup"><span data-stu-id="470b4-115">Example 2: Get all the service objectives by using a server name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

<span data-ttu-id="470b4-116">Questo comando ottiene tutti gli obiettivi di servizio per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="470b4-116">This command gets all the service objectives for the server named Server01.</span></span>

## <span data-ttu-id="470b4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="470b4-117">PARAMETERS</span></span>

### <span data-ttu-id="470b4-118">-Contesto</span><span class="sxs-lookup"><span data-stu-id="470b4-118">-Context</span></span>
<span data-ttu-id="470b4-119">Specifica il contesto di connessione di un server.</span><span class="sxs-lookup"><span data-stu-id="470b4-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="470b4-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="470b4-120">-Profile</span></span>
<span data-ttu-id="470b4-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="470b4-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="470b4-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="470b4-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470b4-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="470b4-123">-ServerName</span></span>
<span data-ttu-id="470b4-124">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="470b4-124">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="470b4-125">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="470b4-125">-ServiceObjective</span></span>
<span data-ttu-id="470b4-126">Specifica un oggetto che rappresenta l'obiettivo del servizio ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="470b4-126">Specifies an object that represents the service objective that this cmdlet gets.</span></span>
<span data-ttu-id="470b4-127">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="470b4-127">Valid values are:</span></span> 

- <span data-ttu-id="470b4-128">Base: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="470b4-128">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="470b4-129">Standard (S0): f1173c43-91bd-4AAA-973C-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="470b4-129">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="470b4-130">Standard (S1): 1b1ebd4d-D903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="470b4-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="470b4-131">Standard (S2): 455330e1-00cd-488b-B5FA-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="470b4-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="470b4-132">\* Standard (S3): 789681b8-CA10-4EB0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="470b4-132">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="470b4-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="470b4-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="470b4-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="470b4-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="470b4-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="470b4-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="470b4-136">Premium (P3): a7c4c615-CFB1-464B-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="470b4-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="470b4-137">\* Standard (S3) fa parte del più recente aggiornamento di database SQL V12 (Preview).</span><span class="sxs-lookup"><span data-stu-id="470b4-137">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="470b4-138">Per altre informazioni, vedere [novità di Azure SQL database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) in Azure Library.</span><span class="sxs-lookup"><span data-stu-id="470b4-138">For more information, see [What's New in the Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/`) in the Azure library.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="470b4-139">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="470b4-139">-ServiceObjectiveName</span></span>
<span data-ttu-id="470b4-140">Specifica il nome di un obiettivo di servizio da ottenere.</span><span class="sxs-lookup"><span data-stu-id="470b4-140">Specifies the name of a service objective to get.</span></span>
<span data-ttu-id="470b4-141">I valori validi sono: Basic, S0, S1, S2, S3, P1, P2 e P3.</span><span class="sxs-lookup"><span data-stu-id="470b4-141">Valid values are: Basic, S0, S1, S2, S3, P1, P2, and P3.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470b4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470b4-142">CommonParameters</span></span>
<span data-ttu-id="470b4-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="470b4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470b4-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="470b4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470b4-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="470b4-145">INPUTS</span></span>

### <span data-ttu-id="470b4-146">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="470b4-146">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective</span></span>

## <span data-ttu-id="470b4-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="470b4-147">OUTPUTS</span></span>

### <span data-ttu-id="470b4-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span><span class="sxs-lookup"><span data-stu-id="470b4-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span></span>

## <span data-ttu-id="470b4-149">Note</span><span class="sxs-lookup"><span data-stu-id="470b4-149">NOTES</span></span>

## <span data-ttu-id="470b4-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="470b4-150">RELATED LINKS</span></span>

[<span data-ttu-id="470b4-151">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="470b4-151">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="470b4-152">Ottenere un obiettivo a livello di servizio</span><span class="sxs-lookup"><span data-stu-id="470b4-152">Get Service Level Objective</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[<span data-ttu-id="470b4-153">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="470b4-153">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="470b4-154">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="470b4-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


