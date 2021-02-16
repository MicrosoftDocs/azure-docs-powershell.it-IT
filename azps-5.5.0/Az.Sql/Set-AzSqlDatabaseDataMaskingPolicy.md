---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176766"
---
# <span data-ttu-id="03d2b-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="03d2b-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="03d2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="03d2b-103">Imposta la maschera dati per un database.</span><span class="sxs-lookup"><span data-stu-id="03d2b-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="03d2b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03d2b-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03d2b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03d2b-105">DESCRIPTION</span></span>
<span data-ttu-id="03d2b-106">Il cmdlet **Set-AzSqlDatabaseDataMaskingPolicy** imposta il criterio di maschera dati per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="03d2b-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="03d2b-107">Per usare questo cmdlet, usare i *parametri ResourceGroupName,* *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="03d2b-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="03d2b-108">È possibile impostare il *parametro DataMaskingState* per specificare se le operazioni di maschera dati devono essere abilitate o disabilitate.</span><span class="sxs-lookup"><span data-stu-id="03d2b-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="03d2b-109">Se il cmdlet ha esito positivo e viene usato il *parametro PassThru,* restituisce un oggetto che descrive i criteri di maschera dati correnti oltre agli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="03d2b-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="03d2b-110">Gli identificatori di database includono, ma non limitati a, **ResourceGroupName,** **ServerName** e **DatabaseName.**</span><span class="sxs-lookup"><span data-stu-id="03d2b-110">Database identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, and **DatabaseName**.</span></span>
<span data-ttu-id="03d2b-111">Questo cmdlet è supportato anche dal servizio SQL Server di estensione del database in Azure.</span><span class="sxs-lookup"><span data-stu-id="03d2b-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="03d2b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03d2b-112">EXAMPLES</span></span>

### <span data-ttu-id="03d2b-113">Esempio 1: Impostare i criteri di maschera dati per un database</span><span class="sxs-lookup"><span data-stu-id="03d2b-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="03d2b-114">Questo comando imposta i criteri di maschera dati per un database denominato database01 nel server denominato server01.</span><span class="sxs-lookup"><span data-stu-id="03d2b-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="03d2b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03d2b-115">PARAMETERS</span></span>

### <span data-ttu-id="03d2b-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="03d2b-116">-DatabaseName</span></span>
<span data-ttu-id="03d2b-117">Specifica il nome del database in cui è impostato il criterio.</span><span class="sxs-lookup"><span data-stu-id="03d2b-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="03d2b-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="03d2b-118">-DataMaskingState</span></span>
<span data-ttu-id="03d2b-119">Specifica se l'operazione di maschera dati è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="03d2b-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="03d2b-120">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="03d2b-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03d2b-121">Abilitato</span><span class="sxs-lookup"><span data-stu-id="03d2b-121">Enabled</span></span>
- <span data-ttu-id="03d2b-122">Disabilitato Il valore predefinito è Abilitato.</span><span class="sxs-lookup"><span data-stu-id="03d2b-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03d2b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d2b-123">-DefaultProfile</span></span>
<span data-ttu-id="03d2b-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="03d2b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03d2b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03d2b-125">-PassThru</span></span>
<span data-ttu-id="03d2b-126">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="03d2b-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03d2b-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="03d2b-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03d2b-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="03d2b-128">-PrivilegedUsers</span></span>
<span data-ttu-id="03d2b-129">Specifica un elenco di ID utente con privilegi separati da punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="03d2b-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="03d2b-130">Questi utenti sono autorizzati a visualizzare i dati mascherati.</span><span class="sxs-lookup"><span data-stu-id="03d2b-130">These users are allowed to view the masking data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03d2b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03d2b-131">-ResourceGroupName</span></span>
<span data-ttu-id="03d2b-132">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="03d2b-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="03d2b-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="03d2b-133">-ServerName</span></span>
<span data-ttu-id="03d2b-134">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="03d2b-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="03d2b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03d2b-135">-Confirm</span></span>
<span data-ttu-id="03d2b-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03d2b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03d2b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03d2b-137">-WhatIf</span></span>
<span data-ttu-id="03d2b-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03d2b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03d2b-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03d2b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03d2b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d2b-140">CommonParameters</span></span>
<span data-ttu-id="03d2b-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03d2b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d2b-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03d2b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d2b-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="03d2b-143">INPUTS</span></span>

### <span data-ttu-id="03d2b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="03d2b-144">System.String</span></span>

## <span data-ttu-id="03d2b-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03d2b-145">OUTPUTS</span></span>

### <span data-ttu-id="03d2b-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="03d2b-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="03d2b-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="03d2b-147">NOTES</span></span>

## <span data-ttu-id="03d2b-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03d2b-148">RELATED LINKS</span></span>

[<span data-ttu-id="03d2b-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="03d2b-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="03d2b-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="03d2b-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="03d2b-151">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="03d2b-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="03d2b-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="03d2b-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="03d2b-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="03d2b-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="03d2b-154">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="03d2b-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


