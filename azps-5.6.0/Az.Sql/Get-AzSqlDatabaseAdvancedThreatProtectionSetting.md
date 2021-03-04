---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 570b56ab98e8679a47bcb26b36f1bea4d24bd275
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993228"
---
# <span data-ttu-id="1d76e-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="1d76e-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="1d76e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d76e-102">SYNOPSIS</span></span>
<span data-ttu-id="1d76e-103">Ottiene le impostazioni di Protezione dalle minacce avanzate per un database.</span><span class="sxs-lookup"><span data-stu-id="1d76e-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="1d76e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d76e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d76e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1d76e-105">DESCRIPTION</span></span>
<span data-ttu-id="1d76e-106">Il cmdlet **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** ottiene le impostazioni di Protezione avanzata dalle minacce di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1d76e-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="1d76e-107">Per usare questo cmdlet, specificare i parametri *ResourceGroupName,* *ServerName* e *DatabaseName* per identificare il database per cui il cmdlet ottiene le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1d76e-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="1d76e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d76e-108">EXAMPLES</span></span>

### <span data-ttu-id="1d76e-109">Esempio 1: Ottenere le impostazioni di Protezione avanzata dalle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="1d76e-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="1d76e-110">Questo comando recupera le impostazioni di Protezione avanzata dalle minacce per un database denominato Database01.</span><span class="sxs-lookup"><span data-stu-id="1d76e-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="1d76e-111">Il database si trova nel server denominato Server01, assegnato al gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1d76e-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="1d76e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d76e-112">PARAMETERS</span></span>

### <span data-ttu-id="1d76e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d76e-113">-DatabaseName</span></span>
<span data-ttu-id="1d76e-114">Specifica il nome di un database.</span><span class="sxs-lookup"><span data-stu-id="1d76e-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="1d76e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d76e-115">-DefaultProfile</span></span>
<span data-ttu-id="1d76e-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1d76e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d76e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d76e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d76e-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="1d76e-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1d76e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1d76e-119">-ServerName</span></span>
<span data-ttu-id="1d76e-120">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="1d76e-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="1d76e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d76e-121">-Confirm</span></span>
<span data-ttu-id="1d76e-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d76e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d76e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d76e-123">-WhatIf</span></span>
<span data-ttu-id="1d76e-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d76e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d76e-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d76e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d76e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d76e-126">CommonParameters</span></span>
<span data-ttu-id="1d76e-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d76e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d76e-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d76e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d76e-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="1d76e-129">INPUTS</span></span>

### <span data-ttu-id="1d76e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1d76e-130">System.String</span></span>

## <span data-ttu-id="1d76e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d76e-131">OUTPUTS</span></span>

### <span data-ttu-id="1d76e-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="1d76e-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="1d76e-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="1d76e-133">NOTES</span></span>

## <span data-ttu-id="1d76e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d76e-134">RELATED LINKS</span></span>

[<span data-ttu-id="1d76e-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="1d76e-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)



