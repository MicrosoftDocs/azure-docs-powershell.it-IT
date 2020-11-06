---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ec35e0ebd0f674c66b7708289c33253b28219433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520586"
---
# <span data-ttu-id="021a4-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="021a4-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="021a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="021a4-102">SYNOPSIS</span></span>
<span data-ttu-id="021a4-103">Modifica la proprietà transparent per un database.</span><span class="sxs-lookup"><span data-stu-id="021a4-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="021a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="021a4-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="021a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="021a4-105">DESCRIPTION</span></span>
<span data-ttu-id="021a4-106">Il cmdlet **set-AzureRmSqlDatabaseTransparentDataEncryption** modifica la proprietà Transparent Data Encryption (SecurityTransparent) di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="021a4-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="021a4-107">Per altre informazioni, Vedi crittografia dei dati trasparente con Azure SQL database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) nella raccolta di Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="021a4-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="021a4-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="021a4-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="021a4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="021a4-109">EXAMPLES</span></span>

### <span data-ttu-id="021a4-110">Esempio 1: abilitare l'attivazione di Transparent per un database</span><span class="sxs-lookup"><span data-stu-id="021a4-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="021a4-111">Questo comando consente a Transparent per il database denominato Database01 sul server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="021a4-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="021a4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="021a4-112">PARAMETERS</span></span>

### <span data-ttu-id="021a4-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="021a4-113">-DatabaseName</span></span>
<span data-ttu-id="021a4-114">Specifica il nome del database modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021a4-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="021a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021a4-115">-DefaultProfile</span></span>
<span data-ttu-id="021a4-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="021a4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="021a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="021a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="021a4-118">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="021a4-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="021a4-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="021a4-119">-ServerName</span></span>
<span data-ttu-id="021a4-120">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="021a4-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="021a4-121">-Stato</span><span class="sxs-lookup"><span data-stu-id="021a4-121">-State</span></span>
<span data-ttu-id="021a4-122">Specifica il valore della proprietà transparent.</span><span class="sxs-lookup"><span data-stu-id="021a4-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="021a4-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="021a4-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="021a4-124">Abilitato</span><span class="sxs-lookup"><span data-stu-id="021a4-124">Enabled</span></span> 
- <span data-ttu-id="021a4-125">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="021a4-125">Disabled</span></span>

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

### <span data-ttu-id="021a4-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="021a4-126">-Confirm</span></span>
<span data-ttu-id="021a4-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021a4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="021a4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="021a4-128">-WhatIf</span></span>
<span data-ttu-id="021a4-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="021a4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="021a4-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="021a4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="021a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021a4-131">CommonParameters</span></span>
<span data-ttu-id="021a4-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="021a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021a4-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="021a4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021a4-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="021a4-134">INPUTS</span></span>

### <span data-ttu-id="021a4-135">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="021a4-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="021a4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="021a4-136">System.String</span></span>

## <span data-ttu-id="021a4-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="021a4-137">OUTPUTS</span></span>

### <span data-ttu-id="021a4-138">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="021a4-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="021a4-139">Note</span><span class="sxs-lookup"><span data-stu-id="021a4-139">NOTES</span></span>

## <span data-ttu-id="021a4-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="021a4-140">RELATED LINKS</span></span>

[<span data-ttu-id="021a4-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="021a4-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="021a4-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="021a4-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="021a4-143">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="021a4-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


