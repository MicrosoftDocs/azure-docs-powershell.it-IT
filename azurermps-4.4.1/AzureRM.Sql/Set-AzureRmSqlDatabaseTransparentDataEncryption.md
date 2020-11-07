---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ca3ee787e577eabc9e889cbb471fcf3a00a4736c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685856"
---
# <span data-ttu-id="367f0-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="367f0-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="367f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="367f0-102">SYNOPSIS</span></span>
<span data-ttu-id="367f0-103">Modifica la proprietà transparent per un database.</span><span class="sxs-lookup"><span data-stu-id="367f0-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="367f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="367f0-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="367f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="367f0-105">DESCRIPTION</span></span>
<span data-ttu-id="367f0-106">Il cmdlet **set-AzureRmSqlDatabaseTransparentDataEncryption** modifica la proprietà Transparent Data Encryption (SecurityTransparent) di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="367f0-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="367f0-107">Per altre informazioni, Vedi crittografia dei dati trasparente con Azure SQL database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) nella raccolta di Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="367f0-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="367f0-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="367f0-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="367f0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="367f0-109">EXAMPLES</span></span>

### <span data-ttu-id="367f0-110">Esempio 1: abilitare l'attivazione di Transparent per un database</span><span class="sxs-lookup"><span data-stu-id="367f0-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="367f0-111">Questo comando consente a Transparent per il database denominato Database01 sul server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="367f0-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="367f0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="367f0-112">PARAMETERS</span></span>

### <span data-ttu-id="367f0-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="367f0-113">-DatabaseName</span></span>
<span data-ttu-id="367f0-114">Specifica il nome del database modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="367f0-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="367f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="367f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="367f0-116">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="367f0-116">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="367f0-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="367f0-117">-ServerName</span></span>
<span data-ttu-id="367f0-118">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="367f0-118">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="367f0-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="367f0-119">-State</span></span>
<span data-ttu-id="367f0-120">Specifica il valore della proprietà transparent.</span><span class="sxs-lookup"><span data-stu-id="367f0-120">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="367f0-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="367f0-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="367f0-122">Abilitato</span><span class="sxs-lookup"><span data-stu-id="367f0-122">Enabled</span></span> 
- <span data-ttu-id="367f0-123">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="367f0-123">Disabled</span></span>

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

### <span data-ttu-id="367f0-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="367f0-124">-Confirm</span></span>
<span data-ttu-id="367f0-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="367f0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="367f0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="367f0-126">-WhatIf</span></span>
<span data-ttu-id="367f0-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="367f0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="367f0-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="367f0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="367f0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367f0-129">-DefaultProfile</span></span>
<span data-ttu-id="367f0-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="367f0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="367f0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367f0-131">CommonParameters</span></span>
<span data-ttu-id="367f0-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="367f0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367f0-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367f0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367f0-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="367f0-134">INPUTS</span></span>

## <span data-ttu-id="367f0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="367f0-135">OUTPUTS</span></span>

### <span data-ttu-id="367f0-136">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="367f0-136">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="367f0-137">Note</span><span class="sxs-lookup"><span data-stu-id="367f0-137">NOTES</span></span>

## <span data-ttu-id="367f0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="367f0-138">RELATED LINKS</span></span>

[<span data-ttu-id="367f0-139">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="367f0-139">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="367f0-140">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="367f0-140">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="367f0-141">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="367f0-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


