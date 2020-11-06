---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: 51e2c480b9a374136f2b040b8884cf85949b5fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517927"
---
# <span data-ttu-id="dfb25-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dfb25-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="dfb25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfb25-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb25-103">Ottiene i criteri di connessione sicura per un database.</span><span class="sxs-lookup"><span data-stu-id="dfb25-103">Gets the secure connection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfb25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfb25-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfb25-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfb25-105">DESCRIPTION</span></span>
<span data-ttu-id="dfb25-106">Il cmdlet **Get-AzureRmSqlDatabaseSecureConnectionPolicy** ottiene i criteri per i canali crittografati di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb25-106">The **Get-AzureRmSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="dfb25-107">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="dfb25-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="dfb25-108">Dopo l'esecuzione di questo cmdlet, viene restituito un oggetto che descrive i criteri di canale crittografati correnti e anche gli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="dfb25-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="dfb25-109">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="dfb25-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="dfb25-110">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb25-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="dfb25-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfb25-111">EXAMPLES</span></span>

### <span data-ttu-id="dfb25-112">Esempio 1: ottenere i criteri per i canali crittografati di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="dfb25-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="dfb25-113">Questo comando consente di ottenere i criteri di canale crittografati di un database SQL di Azure denominato Database01 situato nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="dfb25-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="dfb25-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfb25-114">PARAMETERS</span></span>

### <span data-ttu-id="dfb25-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dfb25-115">-DatabaseName</span></span>
<span data-ttu-id="dfb25-116">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="dfb25-116">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb25-117">-DefaultProfile</span></span>
<span data-ttu-id="dfb25-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dfb25-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfb25-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfb25-119">-ResourceGroupName</span></span>
<span data-ttu-id="dfb25-120">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="dfb25-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="dfb25-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="dfb25-121">-ServerName</span></span>
<span data-ttu-id="dfb25-122">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="dfb25-122">Specifies the name of server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb25-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dfb25-123">-Confirm</span></span>
<span data-ttu-id="dfb25-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb25-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb25-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb25-125">-WhatIf</span></span>
<span data-ttu-id="dfb25-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfb25-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfb25-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfb25-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb25-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb25-128">CommonParameters</span></span>
<span data-ttu-id="dfb25-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfb25-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb25-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfb25-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb25-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfb25-131">INPUTS</span></span>

### <span data-ttu-id="dfb25-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dfb25-132">None</span></span>
<span data-ttu-id="dfb25-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="dfb25-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dfb25-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfb25-134">OUTPUTS</span></span>

### <span data-ttu-id="dfb25-135">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="dfb25-135">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="dfb25-136">Note</span><span class="sxs-lookup"><span data-stu-id="dfb25-136">NOTES</span></span>

## <span data-ttu-id="dfb25-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfb25-137">RELATED LINKS</span></span>
