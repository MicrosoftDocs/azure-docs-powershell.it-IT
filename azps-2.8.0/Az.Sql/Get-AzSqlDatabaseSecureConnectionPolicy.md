---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: d160e6cf954240495a9f9b3969d87dab6d880e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857022"
---
# <span data-ttu-id="a0e51-101">Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a0e51-101">Get-AzSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="a0e51-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0e51-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e51-103">Ottiene i criteri di connessione sicura per un database.</span><span class="sxs-lookup"><span data-stu-id="a0e51-103">Gets the secure connection policy for a database.</span></span> <span data-ttu-id="a0e51-104">La connessione sicura è deprecata e questo comando verrà rimosso in una versione futura.</span><span class="sxs-lookup"><span data-stu-id="a0e51-104">Secure connection is deprecated and this command will be removed in a future release.</span></span> <span data-ttu-id="a0e51-105">Usare la lama database SQL in Azure Portal per visualizzare le stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="a0e51-105">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

## <span data-ttu-id="a0e51-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0e51-106">SYNTAX</span></span>

```
Get-AzSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0e51-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0e51-107">DESCRIPTION</span></span>
<span data-ttu-id="a0e51-108">Il cmdlet **Get-AzSqlDatabaseSecureConnectionPolicy** ottiene i criteri per i canali crittografati di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a0e51-108">The **Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="a0e51-109">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="a0e51-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a0e51-110">Dopo l'esecuzione di questo cmdlet, viene restituito un oggetto che descrive i criteri di canale crittografati correnti e anche gli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="a0e51-110">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="a0e51-111">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="a0e51-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="a0e51-112">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="a0e51-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a0e51-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0e51-113">EXAMPLES</span></span>

### <span data-ttu-id="a0e51-114">Esempio 1: ottenere i criteri per i canali crittografati di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="a0e51-114">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="a0e51-115">Questo comando consente di ottenere i criteri di canale crittografati di un database SQL di Azure denominato Database01 situato nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="a0e51-115">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="a0e51-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0e51-116">PARAMETERS</span></span>

### <span data-ttu-id="a0e51-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0e51-117">-DatabaseName</span></span>
<span data-ttu-id="a0e51-118">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="a0e51-118">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e51-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e51-119">-DefaultProfile</span></span>
<span data-ttu-id="a0e51-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a0e51-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0e51-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e51-121">-ResourceGroupName</span></span>
<span data-ttu-id="a0e51-122">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="a0e51-122">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e51-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a0e51-123">-ServerName</span></span>
<span data-ttu-id="a0e51-124">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="a0e51-124">Specifies the name of server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e51-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0e51-125">-Confirm</span></span>
<span data-ttu-id="a0e51-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0e51-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e51-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e51-127">-WhatIf</span></span>
<span data-ttu-id="a0e51-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0e51-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0e51-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0e51-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e51-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e51-130">CommonParameters</span></span>
<span data-ttu-id="a0e51-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0e51-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e51-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0e51-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e51-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0e51-133">INPUTS</span></span>

### <span data-ttu-id="a0e51-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a0e51-134">System.String</span></span>

## <span data-ttu-id="a0e51-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0e51-135">OUTPUTS</span></span>

### <span data-ttu-id="a0e51-136">Microsoft. Azure. Commands. SQL. SecureConnection. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a0e51-136">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="a0e51-137">Note</span><span class="sxs-lookup"><span data-stu-id="a0e51-137">NOTES</span></span>

## <span data-ttu-id="a0e51-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0e51-138">RELATED LINKS</span></span>
