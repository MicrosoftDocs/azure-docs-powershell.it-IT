---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: ec7c452939d82b82deed507c667bdc9cdeab3cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517915"
---
# <span data-ttu-id="a8eaf-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="a8eaf-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="a8eaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="a8eaf-103">Ottiene lo stato di avanzamento di un'analisi di un database.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-103">Gets the progress of a TDE scan of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8eaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8eaf-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8eaf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8eaf-105">DESCRIPTION</span></span>
<span data-ttu-id="a8eaf-106">Il cmdlet **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** ottiene lo stato di avanzamento di un'analisi di crittografia dei dati trasparente (Transparent Data Encryption) di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="a8eaf-107">Se non è in esecuzione alcun intervallo di crittografia, questo cmdlet restituisce un elenco vuoto.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="a8eaf-108">Per altre informazioni, Vedi crittografia dei dati trasparente con Azure SQL database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) nella raccolta di Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="a8eaf-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="a8eaf-109">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a8eaf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8eaf-110">EXAMPLES</span></span>

### <span data-ttu-id="a8eaf-111">Esempio 1: ottenere l'attività di Transparent per un database</span><span class="sxs-lookup"><span data-stu-id="a8eaf-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="a8eaf-112">Questo comando consente di ottenere l'attività di Transparent per il database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="a8eaf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8eaf-113">PARAMETERS</span></span>

### <span data-ttu-id="a8eaf-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a8eaf-114">-DatabaseName</span></span>
<span data-ttu-id="a8eaf-115">Specifica il nome del database per cui questo cmdlet ottiene l'attività di crittografia di Transcript.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="a8eaf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8eaf-116">-DefaultProfile</span></span>
<span data-ttu-id="a8eaf-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a8eaf-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8eaf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8eaf-118">-ResourceGroupName</span></span>
<span data-ttu-id="a8eaf-119">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a8eaf-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a8eaf-120">-ServerName</span></span>
<span data-ttu-id="a8eaf-121">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a8eaf-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8eaf-122">-Confirm</span></span>
<span data-ttu-id="a8eaf-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8eaf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8eaf-124">-WhatIf</span></span>
<span data-ttu-id="a8eaf-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8eaf-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8eaf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8eaf-127">CommonParameters</span></span>
<span data-ttu-id="a8eaf-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8eaf-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8eaf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8eaf-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8eaf-130">INPUTS</span></span>

### <span data-ttu-id="a8eaf-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a8eaf-131">None</span></span>
<span data-ttu-id="a8eaf-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a8eaf-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8eaf-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8eaf-133">OUTPUTS</span></span>

### <span data-ttu-id="a8eaf-134">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="a8eaf-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="a8eaf-135">Note</span><span class="sxs-lookup"><span data-stu-id="a8eaf-135">NOTES</span></span>

## <span data-ttu-id="a8eaf-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8eaf-136">RELATED LINKS</span></span>

[<span data-ttu-id="a8eaf-137">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="a8eaf-137">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="a8eaf-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="a8eaf-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)


