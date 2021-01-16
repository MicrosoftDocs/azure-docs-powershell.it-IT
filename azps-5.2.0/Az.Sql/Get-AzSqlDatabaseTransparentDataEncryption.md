---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 632b7710a6055f40c6cdc6d87d4b2cf8e3e17eeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371976"
---
# <span data-ttu-id="77bbe-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="77bbe-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="77bbe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="77bbe-103">Ottiene lo stato di Transparence per un database.</span><span class="sxs-lookup"><span data-stu-id="77bbe-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="77bbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77bbe-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77bbe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77bbe-105">DESCRIPTION</span></span>
<span data-ttu-id="77bbe-106">Il cmdlet **Get-AzSqlDatabaseTransparentDataEncryption** ottiene lo stato della crittografia dei dati trasparente (Transparent Data Encryption) per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="77bbe-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="77bbe-107">Per altre informazioni, Vedi crittografia dei dati trasparente con Azure SQL database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) nella raccolta di Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="77bbe-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="77bbe-108">Questo cmdlet ottiene lo stato corrente di Transparent, ma sia la crittografia che la decrittografia possono essere operazioni a esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="77bbe-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="77bbe-109">Per visualizzare lo stato di analisi della crittografia, eseguire il cmdlet Get-AzSqlDatabaseTransparentDataEncryptionActivity.</span><span class="sxs-lookup"><span data-stu-id="77bbe-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="77bbe-110">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="77bbe-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="77bbe-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77bbe-111">EXAMPLES</span></span>

### <span data-ttu-id="77bbe-112">Esempio 1: ottenere lo stato di transparenza per un database</span><span class="sxs-lookup"><span data-stu-id="77bbe-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="77bbe-113">Questo comando ottiene lo stato di Transparent per il database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="77bbe-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="77bbe-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77bbe-114">PARAMETERS</span></span>

### <span data-ttu-id="77bbe-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="77bbe-115">-DatabaseName</span></span>
<span data-ttu-id="77bbe-116">Specifica il nome del database per cui questo cmdlet ottiene lo stato di transparenza.</span><span class="sxs-lookup"><span data-stu-id="77bbe-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="77bbe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77bbe-117">-DefaultProfile</span></span>
<span data-ttu-id="77bbe-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="77bbe-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77bbe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77bbe-119">-ResourceGroupName</span></span>
<span data-ttu-id="77bbe-120">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="77bbe-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="77bbe-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="77bbe-121">-ServerName</span></span>
<span data-ttu-id="77bbe-122">Specifica il nome del server che ospita il database per il quale questo cmdlet ottiene lo stato di tipo Transparent.</span><span class="sxs-lookup"><span data-stu-id="77bbe-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="77bbe-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="77bbe-123">-Confirm</span></span>
<span data-ttu-id="77bbe-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77bbe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77bbe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77bbe-125">-WhatIf</span></span>
<span data-ttu-id="77bbe-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77bbe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77bbe-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77bbe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77bbe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77bbe-128">CommonParameters</span></span>
<span data-ttu-id="77bbe-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77bbe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77bbe-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77bbe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77bbe-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77bbe-131">INPUTS</span></span>

### <span data-ttu-id="77bbe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="77bbe-132">System.String</span></span>

## <span data-ttu-id="77bbe-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77bbe-133">OUTPUTS</span></span>

### <span data-ttu-id="77bbe-134">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="77bbe-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="77bbe-135">Note</span><span class="sxs-lookup"><span data-stu-id="77bbe-135">NOTES</span></span>

## <span data-ttu-id="77bbe-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77bbe-136">RELATED LINKS</span></span>

[<span data-ttu-id="77bbe-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="77bbe-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="77bbe-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="77bbe-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
