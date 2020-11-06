---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 26d056b5ad9cdff22f0419f90fad17c3147e0e14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512163"
---
# <span data-ttu-id="df06b-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="df06b-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="df06b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df06b-102">SYNOPSIS</span></span>
<span data-ttu-id="df06b-103">Imposta la mascheratura dei dati per un database.</span><span class="sxs-lookup"><span data-stu-id="df06b-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df06b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df06b-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df06b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df06b-105">DESCRIPTION</span></span>
<span data-ttu-id="df06b-106">Il cmdlet **set-AzureRmSqlDatabaseDataMaskingPolicy** imposta i criteri per la mascheratura dei dati per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="df06b-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="df06b-107">Per usare questo cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="df06b-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="df06b-108">Puoi impostare il parametro *DataMaskingState* per specificare se le operazioni di mascheramento dei dati sono abilitate o disabilitate.</span><span class="sxs-lookup"><span data-stu-id="df06b-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>

<span data-ttu-id="df06b-109">Puoi anche impostare il parametro *PrivilegedLogins* per specificare gli utenti autorizzati a visualizzare i dati smascherati.</span><span class="sxs-lookup"><span data-stu-id="df06b-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="df06b-110">Se il cmdlet riesce e viene usato il parametro *PassThru* , viene restituito un oggetto che descrive i criteri di mascheramento dei dati correnti oltre agli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="df06b-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="df06b-111">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="df06b-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="df06b-112">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="df06b-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="df06b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df06b-113">EXAMPLES</span></span>

### <span data-ttu-id="df06b-114">Esempio 1: impostare i criteri di mascheramento dei dati per un database</span><span class="sxs-lookup"><span data-stu-id="df06b-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="df06b-115">Questo comando imposta i criteri di mascheramento dei dati per un database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="df06b-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="df06b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df06b-116">PARAMETERS</span></span>

### <span data-ttu-id="df06b-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="df06b-117">-DatabaseName</span></span>
<span data-ttu-id="df06b-118">Specifica il nome del database in cui è impostato il criterio.</span><span class="sxs-lookup"><span data-stu-id="df06b-118">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="df06b-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="df06b-119">-DataMaskingState</span></span>
<span data-ttu-id="df06b-120">Specifica se l'operazione di mascheramento dei dati è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="df06b-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="df06b-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="df06b-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="df06b-122">Abilitato</span><span class="sxs-lookup"><span data-stu-id="df06b-122">Enabled</span></span>
- <span data-ttu-id="df06b-123">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="df06b-123">Disabled</span></span>

<span data-ttu-id="df06b-124">Il valore predefinito è Enabled.</span><span class="sxs-lookup"><span data-stu-id="df06b-124">The default value is Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df06b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df06b-125">-DefaultProfile</span></span>
<span data-ttu-id="df06b-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="df06b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df06b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df06b-127">-PassThru</span></span>
<span data-ttu-id="df06b-128">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="df06b-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="df06b-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="df06b-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df06b-130">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="df06b-130">-PrivilegedLogins</span></span>
<span data-ttu-id="df06b-131">Specifica gli utenti SQL esclusi dalla maschera.</span><span class="sxs-lookup"><span data-stu-id="df06b-131">Specifies which SQL users are excluded from masking.</span></span>

<span data-ttu-id="df06b-132">Questo parametro è deprecato e verrà rimosso dalle versioni future.</span><span class="sxs-lookup"><span data-stu-id="df06b-132">This parameter is deprecated and will be removed from future releases.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df06b-133">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="df06b-133">-PrivilegedUsers</span></span>
<span data-ttu-id="df06b-134">Specifica un elenco delimitato da punti e virgola di ID utente privilegiati.</span><span class="sxs-lookup"><span data-stu-id="df06b-134">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="df06b-135">Questi utenti possono visualizzare i dati per la mascheratura.</span><span class="sxs-lookup"><span data-stu-id="df06b-135">These users are allowed to view the masking data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df06b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df06b-136">-ResourceGroupName</span></span>
<span data-ttu-id="df06b-137">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="df06b-137">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="df06b-138">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="df06b-138">-ServerName</span></span>
<span data-ttu-id="df06b-139">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="df06b-139">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="df06b-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="df06b-140">-Confirm</span></span>
<span data-ttu-id="df06b-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df06b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df06b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df06b-142">-WhatIf</span></span>
<span data-ttu-id="df06b-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df06b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df06b-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df06b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df06b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df06b-145">CommonParameters</span></span>
<span data-ttu-id="df06b-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df06b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df06b-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df06b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df06b-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df06b-148">INPUTS</span></span>

### <span data-ttu-id="df06b-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="df06b-149">None</span></span>
<span data-ttu-id="df06b-150">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="df06b-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df06b-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df06b-151">OUTPUTS</span></span>

### <span data-ttu-id="df06b-152">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="df06b-152">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="df06b-153">Note</span><span class="sxs-lookup"><span data-stu-id="df06b-153">NOTES</span></span>

## <span data-ttu-id="df06b-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df06b-154">RELATED LINKS</span></span>

[<span data-ttu-id="df06b-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="df06b-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="df06b-156">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="df06b-156">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="df06b-157">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="df06b-157">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="df06b-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="df06b-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="df06b-159">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="df06b-159">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="df06b-160">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="df06b-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


