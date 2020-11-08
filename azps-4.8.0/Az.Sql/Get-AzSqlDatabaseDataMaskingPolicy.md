---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031036"
---
# <span data-ttu-id="5b8a3-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="5b8a3-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="5b8a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b8a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5b8a3-103">Ottiene i criteri di mascheramento dei dati per un database.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="5b8a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b8a3-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b8a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b8a3-105">DESCRIPTION</span></span>
<span data-ttu-id="5b8a3-106">Il cmdlet **Get-AzSqlDatabaseDataMaskingPolicy** ottiene i criteri di mascheramento dei dati di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="5b8a3-107">Per usare questo cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="5b8a3-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5b8a3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b8a3-109">EXAMPLES</span></span>

### <span data-ttu-id="5b8a3-110">Esempio 1: ottenere i criteri di mascheramento dei dati per un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="5b8a3-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="5b8a3-111">Questo comando consente di ottenere i criteri di mascheramento dei dati da database Database01 nel gruppo di risorse ResourceGroup01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="5b8a3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b8a3-112">PARAMETERS</span></span>

### <span data-ttu-id="5b8a3-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5b8a3-113">-DatabaseName</span></span>
<span data-ttu-id="5b8a3-114">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="5b8a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b8a3-115">-DefaultProfile</span></span>
<span data-ttu-id="5b8a3-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5b8a3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b8a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b8a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="5b8a3-118">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5b8a3-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5b8a3-119">-ServerName</span></span>
<span data-ttu-id="5b8a3-120">Specifica il nome del server in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="5b8a3-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b8a3-121">-Confirm</span></span>
<span data-ttu-id="5b8a3-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b8a3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b8a3-123">-WhatIf</span></span>
<span data-ttu-id="5b8a3-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b8a3-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b8a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b8a3-126">CommonParameters</span></span>
<span data-ttu-id="5b8a3-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b8a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b8a3-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b8a3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b8a3-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b8a3-129">INPUTS</span></span>

### <span data-ttu-id="5b8a3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5b8a3-130">System.String</span></span>

## <span data-ttu-id="5b8a3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b8a3-131">OUTPUTS</span></span>

### <span data-ttu-id="5b8a3-132">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5b8a3-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="5b8a3-133">Note</span><span class="sxs-lookup"><span data-stu-id="5b8a3-133">NOTES</span></span>

## <span data-ttu-id="5b8a3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b8a3-134">RELATED LINKS</span></span>

[<span data-ttu-id="5b8a3-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5b8a3-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5b8a3-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5b8a3-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5b8a3-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5b8a3-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5b8a3-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="5b8a3-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="5b8a3-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5b8a3-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


