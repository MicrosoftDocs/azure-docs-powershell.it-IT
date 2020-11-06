---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 8e0c13565641a6033a22545d95af28df1c14a772
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512219"
---
# <span data-ttu-id="45e39-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="45e39-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="45e39-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45e39-102">SYNOPSIS</span></span>
<span data-ttu-id="45e39-103">Rimuove i criteri di rilevamento delle minacce da un database.</span><span class="sxs-lookup"><span data-stu-id="45e39-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45e39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45e39-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45e39-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45e39-105">DESCRIPTION</span></span>
<span data-ttu-id="45e39-106">Il cmdlet **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** rimuove i criteri di rilevamento delle minacce da un database SQL di AzureAzure.</span><span class="sxs-lookup"><span data-stu-id="45e39-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="45e39-107">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* e *ServerName* per identificare il database da cui questo cmdlet rimuove il criterio.</span><span class="sxs-lookup"><span data-stu-id="45e39-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="45e39-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45e39-108">EXAMPLES</span></span>

### <span data-ttu-id="45e39-109">Esempio 1: rimuovere un criterio di rilevamento delle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="45e39-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="45e39-110">Questo comando rimuove i criteri di rilevamento delle minacce da un database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="45e39-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="45e39-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45e39-111">PARAMETERS</span></span>

### <span data-ttu-id="45e39-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45e39-112">-DatabaseName</span></span>
<span data-ttu-id="45e39-113">Specifica il nome di un database in cui devono essere rimossi i criteri di rilevamento delle minacce.</span><span class="sxs-lookup"><span data-stu-id="45e39-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="45e39-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e39-114">-DefaultProfile</span></span>
<span data-ttu-id="45e39-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="45e39-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45e39-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45e39-116">-PassThru</span></span>
<span data-ttu-id="45e39-117">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="45e39-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="45e39-118">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="45e39-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="45e39-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e39-119">-ResourceGroupName</span></span>
<span data-ttu-id="45e39-120">Specifica il nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="45e39-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="45e39-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="45e39-121">-ServerName</span></span>
<span data-ttu-id="45e39-122">Specifica il nome di un server in cui viene eseguito il database.</span><span class="sxs-lookup"><span data-stu-id="45e39-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="45e39-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45e39-123">-Confirm</span></span>
<span data-ttu-id="45e39-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45e39-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e39-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45e39-125">-WhatIf</span></span>
<span data-ttu-id="45e39-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45e39-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45e39-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45e39-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e39-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e39-128">CommonParameters</span></span>
<span data-ttu-id="45e39-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e39-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e39-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45e39-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e39-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45e39-131">INPUTS</span></span>

###  
<span data-ttu-id="45e39-132">Non è possibile reindirizzare l'input a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45e39-132">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="45e39-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45e39-133">OUTPUTS</span></span>

### <span data-ttu-id="45e39-134">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="45e39-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="45e39-135">Questo cmdlet restituisce un oggetto **DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="45e39-135">This cmdlet returns a **DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="45e39-136">Note</span><span class="sxs-lookup"><span data-stu-id="45e39-136">NOTES</span></span>

## <span data-ttu-id="45e39-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45e39-137">RELATED LINKS</span></span>

[<span data-ttu-id="45e39-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="45e39-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


