---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 4abe17fb272e97637bbd43a69401f9c101f14ef6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967582"
---
# <span data-ttu-id="d6f4d-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="d6f4d-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="d6f4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f4d-103">Disabilita Advanced Data Security in un server.</span><span class="sxs-lookup"><span data-stu-id="d6f4d-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="d6f4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6f4d-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6f4d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d6f4d-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f4d-106">Il cmdlet **Disable-AzSqlServerAdvancedDataSecurity** disabilita Advanced Data Security in un server.</span><span class="sxs-lookup"><span data-stu-id="d6f4d-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="d6f4d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6f4d-107">EXAMPLES</span></span>

### <span data-ttu-id="d6f4d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d6f4d-108">Example 1</span></span>
### <span data-ttu-id="d6f4d-109">Esempio 2: Disabilitare Advanced Data Security del server</span><span class="sxs-lookup"><span data-stu-id="d6f4d-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="d6f4d-110">Esempio 3: Disabilitare Advanced Data Security del server dalla risorsa server</span><span class="sxs-lookup"><span data-stu-id="d6f4d-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="d6f4d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6f4d-111">PARAMETERS</span></span>

### <span data-ttu-id="d6f4d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f4d-112">-DefaultProfile</span></span>
<span data-ttu-id="d6f4d-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f4d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6f4d-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6f4d-114">-InputObject</span></span>
<span data-ttu-id="d6f4d-115">Oggetto server da usare con l'operazione dei criteri di Sicurezza dei dati avanzata</span><span class="sxs-lookup"><span data-stu-id="d6f4d-115">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f4d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f4d-116">-ResourceGroupName</span></span>
<span data-ttu-id="d6f4d-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6f4d-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="d6f4d-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d6f4d-118">-ServerName</span></span>
<span data-ttu-id="d6f4d-119">SQL del server di database.</span><span class="sxs-lookup"><span data-stu-id="d6f4d-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="d6f4d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6f4d-120">-Confirm</span></span>
<span data-ttu-id="d6f4d-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6f4d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f4d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f4d-122">-WhatIf</span></span>
<span data-ttu-id="d6f4d-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6f4d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f4d-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6f4d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f4d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f4d-125">CommonParameters</span></span>
<span data-ttu-id="d6f4d-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f4d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f4d-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d6f4d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f4d-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="d6f4d-128">INPUTS</span></span>

### <span data-ttu-id="d6f4d-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="d6f4d-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="d6f4d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d6f4d-130">System.String</span></span>

## <span data-ttu-id="d6f4d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6f4d-131">OUTPUTS</span></span>

### <span data-ttu-id="d6f4d-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d6f4d-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="d6f4d-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="d6f4d-133">NOTES</span></span>

## <span data-ttu-id="d6f4d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6f4d-134">RELATED LINKS</span></span>
