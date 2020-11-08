---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021657"
---
# <span data-ttu-id="b857e-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="b857e-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="b857e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b857e-102">SYNOPSIS</span></span>
<span data-ttu-id="b857e-103">Rimuove le impostazioni avanzate di protezione dalle minacce da un server.</span><span class="sxs-lookup"><span data-stu-id="b857e-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="b857e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b857e-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b857e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b857e-105">DESCRIPTION</span></span>
<span data-ttu-id="b857e-106">Il cmdlet Clear-AzSqlServerAdvancedThreatProtectionSetting consente di rimuovere le impostazioni avanzate di protezione dalle minacce da un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b857e-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="b857e-107">Per usare questo cmdlet, specificare i parametri ResourceGroupName e ServerName per identificare il server da cui questo cmdlet rimuove le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b857e-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="b857e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b857e-108">EXAMPLES</span></span>

### <span data-ttu-id="b857e-109">Esempio 1: rimuovere le impostazioni avanzate di protezione dalle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="b857e-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="b857e-110">Questo comando rimuove le impostazioni avanzate di protezione dalle minacce da un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="b857e-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="b857e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b857e-111">PARAMETERS</span></span>

### <span data-ttu-id="b857e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b857e-112">-DefaultProfile</span></span>
<span data-ttu-id="b857e-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b857e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b857e-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b857e-114">-PassThru</span></span>
<span data-ttu-id="b857e-115">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b857e-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b857e-116">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b857e-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b857e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b857e-117">-ResourceGroupName</span></span>
<span data-ttu-id="b857e-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="b857e-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="b857e-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b857e-119">-ServerName</span></span>
<span data-ttu-id="b857e-120">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="b857e-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b857e-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b857e-121">-Confirm</span></span>
<span data-ttu-id="b857e-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b857e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b857e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b857e-123">-WhatIf</span></span>
<span data-ttu-id="b857e-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b857e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b857e-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b857e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b857e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b857e-126">CommonParameters</span></span>
<span data-ttu-id="b857e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b857e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b857e-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b857e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b857e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b857e-129">INPUTS</span></span>

### <span data-ttu-id="b857e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b857e-130">System.String</span></span>

## <span data-ttu-id="b857e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b857e-131">OUTPUTS</span></span>

### <span data-ttu-id="b857e-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="b857e-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="b857e-133">Note</span><span class="sxs-lookup"><span data-stu-id="b857e-133">NOTES</span></span>

## <span data-ttu-id="b857e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b857e-134">RELATED LINKS</span></span>

[<span data-ttu-id="b857e-135">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="b857e-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

