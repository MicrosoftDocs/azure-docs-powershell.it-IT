---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 976dbc06c71b31ea9058355d55f1eff53681f6e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519683"
---
# <span data-ttu-id="f0575-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="f0575-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="f0575-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0575-102">SYNOPSIS</span></span>
<span data-ttu-id="f0575-103">Ottiene lo stato di Transparence per un database.</span><span class="sxs-lookup"><span data-stu-id="f0575-103">Gets the TDE state for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0575-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0575-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0575-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0575-105">DESCRIPTION</span></span>
<span data-ttu-id="f0575-106">Il cmdlet **Get-AzureRmSqlDatabaseTransparentDataEncryption** ottiene lo stato della crittografia dei dati trasparente (Transparent Data Encryption) per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f0575-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="f0575-107">Per altre informazioni, Vedi crittografia dei dati trasparente con Azure SQL database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) nella raccolta di Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="f0575-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="f0575-108">Questo cmdlet ottiene lo stato corrente di Transparent, ma sia la crittografia che la decrittografia possono essere operazioni a esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="f0575-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="f0575-109">Per visualizzare lo stato di analisi della crittografia, eseguire il cmdlet Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.</span><span class="sxs-lookup"><span data-stu-id="f0575-109">To see the encryption scan progress, run the Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="f0575-110">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="f0575-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f0575-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0575-111">EXAMPLES</span></span>

### <span data-ttu-id="f0575-112">Esempio 1: ottenere lo stato di transparenza per un database</span><span class="sxs-lookup"><span data-stu-id="f0575-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="f0575-113">Questo comando ottiene lo stato di Transparent per il database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="f0575-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="f0575-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0575-114">PARAMETERS</span></span>

### <span data-ttu-id="f0575-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f0575-115">-DatabaseName</span></span>
<span data-ttu-id="f0575-116">Specifica il nome del database per cui questo cmdlet ottiene lo stato di transparenza.</span><span class="sxs-lookup"><span data-stu-id="f0575-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="f0575-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0575-117">-DefaultProfile</span></span>
<span data-ttu-id="f0575-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f0575-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0575-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0575-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0575-120">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="f0575-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f0575-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f0575-121">-ServerName</span></span>
<span data-ttu-id="f0575-122">Specifica il nome del server che ospita il database per il quale questo cmdlet ottiene lo stato di tipo Transparent.</span><span class="sxs-lookup"><span data-stu-id="f0575-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="f0575-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0575-123">-Confirm</span></span>
<span data-ttu-id="f0575-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0575-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0575-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0575-125">-WhatIf</span></span>
<span data-ttu-id="f0575-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0575-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0575-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0575-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0575-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0575-128">CommonParameters</span></span>
<span data-ttu-id="f0575-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0575-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0575-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0575-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0575-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0575-131">INPUTS</span></span>

### <span data-ttu-id="f0575-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f0575-132">System.String</span></span>

## <span data-ttu-id="f0575-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0575-133">OUTPUTS</span></span>

### <span data-ttu-id="f0575-134">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="f0575-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="f0575-135">Note</span><span class="sxs-lookup"><span data-stu-id="f0575-135">NOTES</span></span>

## <span data-ttu-id="f0575-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0575-136">RELATED LINKS</span></span>

[<span data-ttu-id="f0575-137">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="f0575-137">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="f0575-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="f0575-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)
