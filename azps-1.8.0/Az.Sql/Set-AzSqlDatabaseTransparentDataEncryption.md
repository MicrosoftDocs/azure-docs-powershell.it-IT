---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 8d89b966da0fc9d5f0517c5faf777cb5d16efc33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676738"
---
# <span data-ttu-id="d34e2-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="d34e2-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="d34e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d34e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d34e2-103">Modifica la proprietà transparent per un database.</span><span class="sxs-lookup"><span data-stu-id="d34e2-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="d34e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d34e2-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d34e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d34e2-105">DESCRIPTION</span></span>
<span data-ttu-id="d34e2-106">Il cmdlet **set-AzSqlDatabaseTransparentDataEncryption** modifica la proprietà Transparent Data Encryption (SecurityTransparent) di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d34e2-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="d34e2-107">Per altre informazioni, Vedi crittografia dei dati trasparente con Azure SQL database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) nella raccolta di Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="d34e2-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="d34e2-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="d34e2-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d34e2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d34e2-109">EXAMPLES</span></span>

### <span data-ttu-id="d34e2-110">Esempio 1: abilitare l'attivazione di Transparent per un database</span><span class="sxs-lookup"><span data-stu-id="d34e2-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="d34e2-111">Questo comando consente a Transparent per il database denominato Database01 sul server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="d34e2-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="d34e2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d34e2-112">PARAMETERS</span></span>

### <span data-ttu-id="d34e2-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d34e2-113">-DatabaseName</span></span>
<span data-ttu-id="d34e2-114">Specifica il nome del database modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d34e2-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d34e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34e2-115">-DefaultProfile</span></span>
<span data-ttu-id="d34e2-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d34e2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d34e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="d34e2-118">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="d34e2-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d34e2-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="d34e2-119">-ServerName</span></span>
<span data-ttu-id="d34e2-120">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="d34e2-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d34e2-121">-Stato</span><span class="sxs-lookup"><span data-stu-id="d34e2-121">-State</span></span>
<span data-ttu-id="d34e2-122">Specifica il valore della proprietà transparent.</span><span class="sxs-lookup"><span data-stu-id="d34e2-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="d34e2-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d34e2-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d34e2-124">Abilitato</span><span class="sxs-lookup"><span data-stu-id="d34e2-124">Enabled</span></span> 
- <span data-ttu-id="d34e2-125">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="d34e2-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34e2-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d34e2-126">-Confirm</span></span>
<span data-ttu-id="d34e2-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d34e2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d34e2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d34e2-128">-WhatIf</span></span>
<span data-ttu-id="d34e2-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d34e2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d34e2-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d34e2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d34e2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34e2-131">CommonParameters</span></span>
<span data-ttu-id="d34e2-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d34e2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34e2-133">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d34e2-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34e2-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d34e2-134">INPUTS</span></span>

### <span data-ttu-id="d34e2-135">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="d34e2-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="d34e2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d34e2-136">System.String</span></span>

## <span data-ttu-id="d34e2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d34e2-137">OUTPUTS</span></span>

### <span data-ttu-id="d34e2-138">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="d34e2-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="d34e2-139">Note</span><span class="sxs-lookup"><span data-stu-id="d34e2-139">NOTES</span></span>

## <span data-ttu-id="d34e2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d34e2-140">RELATED LINKS</span></span>

[<span data-ttu-id="d34e2-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="d34e2-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="d34e2-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="d34e2-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="d34e2-143">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="d34e2-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


