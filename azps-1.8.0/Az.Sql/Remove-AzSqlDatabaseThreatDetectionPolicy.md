---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: b0ca96910d763cfcf40530ad99872e1e0d50ca31
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676809"
---
# <span data-ttu-id="6091c-101">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6091c-101">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="6091c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6091c-102">SYNOPSIS</span></span>
<span data-ttu-id="6091c-103">Rimuove i criteri di rilevamento delle minacce da un database.</span><span class="sxs-lookup"><span data-stu-id="6091c-103">Removes the threat detection policy from a database.</span></span>

## <span data-ttu-id="6091c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6091c-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6091c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6091c-105">DESCRIPTION</span></span>
<span data-ttu-id="6091c-106">Il cmdlet **Remove-AzSqlDatabaseThreatDetectionPolicy** rimuove i criteri di rilevamento delle minacce da un database SQL di AzureAzure.</span><span class="sxs-lookup"><span data-stu-id="6091c-106">The **Remove-AzSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="6091c-107">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* e *ServerName* per identificare il database da cui questo cmdlet rimuove il criterio.</span><span class="sxs-lookup"><span data-stu-id="6091c-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="6091c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6091c-108">EXAMPLES</span></span>

### <span data-ttu-id="6091c-109">Esempio 1: rimuovere un criterio di rilevamento delle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="6091c-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="6091c-110">Questo comando rimuove i criteri di rilevamento delle minacce da un database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="6091c-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="6091c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6091c-111">PARAMETERS</span></span>

### <span data-ttu-id="6091c-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6091c-112">-DatabaseName</span></span>
<span data-ttu-id="6091c-113">Specifica il nome di un database in cui devono essere rimossi i criteri di rilevamento delle minacce.</span><span class="sxs-lookup"><span data-stu-id="6091c-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="6091c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6091c-114">-DefaultProfile</span></span>
<span data-ttu-id="6091c-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6091c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6091c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6091c-116">-PassThru</span></span>
<span data-ttu-id="6091c-117">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="6091c-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6091c-118">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="6091c-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6091c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6091c-119">-ResourceGroupName</span></span>
<span data-ttu-id="6091c-120">Specifica il nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="6091c-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="6091c-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6091c-121">-ServerName</span></span>
<span data-ttu-id="6091c-122">Specifica il nome di un server in cui viene eseguito il database.</span><span class="sxs-lookup"><span data-stu-id="6091c-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="6091c-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6091c-123">-Confirm</span></span>
<span data-ttu-id="6091c-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6091c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6091c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6091c-125">-WhatIf</span></span>
<span data-ttu-id="6091c-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6091c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6091c-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6091c-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6091c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6091c-128">CommonParameters</span></span>
<span data-ttu-id="6091c-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6091c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6091c-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6091c-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6091c-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6091c-131">INPUTS</span></span>

### <span data-ttu-id="6091c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6091c-132">System.String</span></span>

## <span data-ttu-id="6091c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6091c-133">OUTPUTS</span></span>

### <span data-ttu-id="6091c-134">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="6091c-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="6091c-135">Note</span><span class="sxs-lookup"><span data-stu-id="6091c-135">NOTES</span></span>

## <span data-ttu-id="6091c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6091c-136">RELATED LINKS</span></span>

[<span data-ttu-id="6091c-137">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="6091c-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


