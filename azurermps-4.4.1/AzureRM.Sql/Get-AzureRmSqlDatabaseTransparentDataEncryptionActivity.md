---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: 0f858e2ad0260995b71ec6146a6ce7e64bd48c29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685731"
---
# <span data-ttu-id="4ed09-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="4ed09-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="4ed09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ed09-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed09-103">Ottiene lo stato di avanzamento di un'analisi di un database.</span><span class="sxs-lookup"><span data-stu-id="4ed09-103">Gets the progress of a TDE scan of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ed09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ed09-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ed09-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ed09-105">DESCRIPTION</span></span>
<span data-ttu-id="4ed09-106">Il cmdlet **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** ottiene lo stato di avanzamento di un'analisi di crittografia dei dati trasparente (Transparent Data Encryption) di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed09-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="4ed09-107">Se non è in esecuzione alcun intervallo di crittografia, questo cmdlet restituisce un elenco vuoto.</span><span class="sxs-lookup"><span data-stu-id="4ed09-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="4ed09-108">Per altre informazioni, Vedi crittografia dei dati trasparente con Azure SQL database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) nella raccolta di Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="4ed09-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="4ed09-109">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed09-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4ed09-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ed09-110">EXAMPLES</span></span>

### <span data-ttu-id="4ed09-111">Esempio 1: ottenere l'attività di Transparent per un database</span><span class="sxs-lookup"><span data-stu-id="4ed09-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="4ed09-112">Questo comando consente di ottenere l'attività di Transparent per il database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="4ed09-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="4ed09-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ed09-113">PARAMETERS</span></span>

### <span data-ttu-id="4ed09-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ed09-114">-DatabaseName</span></span>
<span data-ttu-id="4ed09-115">Specifica il nome del database per cui questo cmdlet ottiene l'attività di crittografia di Transcript.</span><span class="sxs-lookup"><span data-stu-id="4ed09-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="4ed09-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed09-116">-ResourceGroupName</span></span>
<span data-ttu-id="4ed09-117">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="4ed09-117">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4ed09-118">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4ed09-118">-ServerName</span></span>
<span data-ttu-id="4ed09-119">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="4ed09-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="4ed09-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ed09-120">-Confirm</span></span>
<span data-ttu-id="4ed09-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed09-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed09-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed09-122">-WhatIf</span></span>
<span data-ttu-id="4ed09-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ed09-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed09-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ed09-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed09-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed09-125">-DefaultProfile</span></span>
<span data-ttu-id="4ed09-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed09-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ed09-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed09-127">CommonParameters</span></span>
<span data-ttu-id="4ed09-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed09-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed09-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed09-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed09-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ed09-130">INPUTS</span></span>

## <span data-ttu-id="4ed09-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ed09-131">OUTPUTS</span></span>

### <span data-ttu-id="4ed09-132">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="4ed09-132">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="4ed09-133">Note</span><span class="sxs-lookup"><span data-stu-id="4ed09-133">NOTES</span></span>

## <span data-ttu-id="4ed09-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ed09-134">RELATED LINKS</span></span>

[<span data-ttu-id="4ed09-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4ed09-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="4ed09-136">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4ed09-136">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)


