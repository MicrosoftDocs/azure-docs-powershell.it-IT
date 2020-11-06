---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d59891980c11b90ee73275dbccb6a98b65c89613
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510811"
---
# <span data-ttu-id="77b83-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="77b83-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="77b83-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77b83-102">SYNOPSIS</span></span>
<span data-ttu-id="77b83-103">Imposta la mascheratura dei dati per un database.</span><span class="sxs-lookup"><span data-stu-id="77b83-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77b83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77b83-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77b83-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77b83-105">DESCRIPTION</span></span>
<span data-ttu-id="77b83-106">Il cmdlet **set-AzureRmSqlDatabaseDataMaskingPolicy** imposta i criteri per la mascheratura dei dati per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="77b83-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="77b83-107">Per usare questo cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="77b83-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="77b83-108">Puoi impostare il parametro *DataMaskingState* per specificare se le operazioni di mascheramento dei dati sono abilitate o disabilitate.</span><span class="sxs-lookup"><span data-stu-id="77b83-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="77b83-109">Puoi anche impostare il parametro *PrivilegedLogins* per specificare gli utenti autorizzati a visualizzare i dati smascherati.</span><span class="sxs-lookup"><span data-stu-id="77b83-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="77b83-110">Se il cmdlet riesce e viene usato il parametro *PassThru* , viene restituito un oggetto che descrive i criteri di mascheramento dei dati correnti oltre agli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="77b83-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="77b83-111">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="77b83-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="77b83-112">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="77b83-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="77b83-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77b83-113">EXAMPLES</span></span>

### <span data-ttu-id="77b83-114">Esempio 1: impostare i criteri di mascheramento dei dati per un database</span><span class="sxs-lookup"><span data-stu-id="77b83-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="77b83-115">Questo comando imposta i criteri di mascheramento dei dati per un database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="77b83-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="77b83-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77b83-116">PARAMETERS</span></span>

### <span data-ttu-id="77b83-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="77b83-117">-DatabaseName</span></span>
<span data-ttu-id="77b83-118">Specifica il nome del database in cui è impostato il criterio.</span><span class="sxs-lookup"><span data-stu-id="77b83-118">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="77b83-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="77b83-119">-DataMaskingState</span></span>
<span data-ttu-id="77b83-120">Specifica se l'operazione di mascheramento dei dati è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="77b83-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="77b83-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="77b83-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77b83-122">Abilitato</span><span class="sxs-lookup"><span data-stu-id="77b83-122">Enabled</span></span>
- <span data-ttu-id="77b83-123">Disabilitato il valore predefinito è abilitato.</span><span class="sxs-lookup"><span data-stu-id="77b83-123">Disabled The default value is Enabled.</span></span>

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

### <span data-ttu-id="77b83-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b83-124">-DefaultProfile</span></span>
<span data-ttu-id="77b83-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="77b83-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77b83-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77b83-126">-PassThru</span></span>
<span data-ttu-id="77b83-127">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="77b83-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="77b83-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="77b83-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="77b83-129">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="77b83-129">-PrivilegedLogins</span></span>
<span data-ttu-id="77b83-130">Specifica gli utenti SQL esclusi dalla maschera.</span><span class="sxs-lookup"><span data-stu-id="77b83-130">Specifies which SQL users are excluded from masking.</span></span>
<span data-ttu-id="77b83-131">Questo parametro è deprecato e verrà rimosso dalle versioni future.</span><span class="sxs-lookup"><span data-stu-id="77b83-131">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="77b83-132">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="77b83-132">-PrivilegedUsers</span></span>
<span data-ttu-id="77b83-133">Specifica un elenco delimitato da punti e virgola di ID utente privilegiati.</span><span class="sxs-lookup"><span data-stu-id="77b83-133">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="77b83-134">Questi utenti possono visualizzare i dati per la mascheratura.</span><span class="sxs-lookup"><span data-stu-id="77b83-134">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="77b83-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77b83-135">-ResourceGroupName</span></span>
<span data-ttu-id="77b83-136">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="77b83-136">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="77b83-137">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="77b83-137">-ServerName</span></span>
<span data-ttu-id="77b83-138">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="77b83-138">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="77b83-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="77b83-139">-Confirm</span></span>
<span data-ttu-id="77b83-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77b83-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77b83-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77b83-141">-WhatIf</span></span>
<span data-ttu-id="77b83-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77b83-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77b83-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77b83-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77b83-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b83-144">CommonParameters</span></span>
<span data-ttu-id="77b83-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b83-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b83-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77b83-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b83-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77b83-147">INPUTS</span></span>

### <span data-ttu-id="77b83-148">System. String</span><span class="sxs-lookup"><span data-stu-id="77b83-148">System.String</span></span>

## <span data-ttu-id="77b83-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77b83-149">OUTPUTS</span></span>

### <span data-ttu-id="77b83-150">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="77b83-150">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="77b83-151">Note</span><span class="sxs-lookup"><span data-stu-id="77b83-151">NOTES</span></span>

## <span data-ttu-id="77b83-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77b83-152">RELATED LINKS</span></span>

[<span data-ttu-id="77b83-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="77b83-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="77b83-154">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="77b83-154">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="77b83-155">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="77b83-155">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="77b83-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="77b83-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="77b83-157">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="77b83-157">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="77b83-158">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="77b83-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

