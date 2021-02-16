---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183302"
---
# <span data-ttu-id="3e54a-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="3e54a-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="3e54a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e54a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e54a-103">Ottiene le impostazioni di Protezione dalle minacce avanzate per un server.</span><span class="sxs-lookup"><span data-stu-id="3e54a-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="3e54a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e54a-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e54a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e54a-105">DESCRIPTION</span></span>
<span data-ttu-id="3e54a-106">Il cmdlet **Get-AzSqlServerAdvancedThreatProtectionSetting** ottiene le impostazioni di Protezione avanzata dalle minacce di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3e54a-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="3e54a-107">Per usare questo cmdlet, specificare i *parametri ResourceGroupName* e *ServerName* per identificare il server per cui il cmdlet ottiene le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="3e54a-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="3e54a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e54a-108">EXAMPLES</span></span>

### <span data-ttu-id="3e54a-109">Esempio 1: Ottenere le impostazioni di Protezione avanzata dalle minacce per un server</span><span class="sxs-lookup"><span data-stu-id="3e54a-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="3e54a-110">Questo comando recupera le impostazioni di Protezione avanzata dalle minacce per un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="3e54a-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="3e54a-111">Il server è assegnato al gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3e54a-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="3e54a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e54a-112">PARAMETERS</span></span>

### <span data-ttu-id="3e54a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e54a-113">-DefaultProfile</span></span>
<span data-ttu-id="3e54a-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="3e54a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e54a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e54a-115">-ResourceGroupName</span></span>
<span data-ttu-id="3e54a-116">Specifica il nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="3e54a-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="3e54a-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3e54a-117">-ServerName</span></span>
<span data-ttu-id="3e54a-118">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="3e54a-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="3e54a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e54a-119">-Confirm</span></span>
<span data-ttu-id="3e54a-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e54a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e54a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e54a-121">-WhatIf</span></span>
<span data-ttu-id="3e54a-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e54a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e54a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e54a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e54a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e54a-124">CommonParameters</span></span>
<span data-ttu-id="3e54a-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e54a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e54a-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e54a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e54a-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e54a-127">INPUTS</span></span>

### <span data-ttu-id="3e54a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3e54a-128">System.String</span></span>

## <span data-ttu-id="3e54a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e54a-129">OUTPUTS</span></span>

### <span data-ttu-id="3e54a-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="3e54a-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="3e54a-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e54a-131">NOTES</span></span>

## <span data-ttu-id="3e54a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e54a-132">RELATED LINKS</span></span>

[<span data-ttu-id="3e54a-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="3e54a-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="3e54a-134">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="3e54a-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


