---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 5dd2c495fa80826f88f96901df7a02ad33bf8e4f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196190"
---
# <span data-ttu-id="fdc4b-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="fdc4b-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="fdc4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdc4b-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc4b-103">Disabilita Advanced Data Security in un server.</span><span class="sxs-lookup"><span data-stu-id="fdc4b-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="fdc4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdc4b-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fdc4b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fdc4b-105">DESCRIPTION</span></span>
<span data-ttu-id="fdc4b-106">Il cmdlet **Disable-AzSqlServerAdvancedDataSecurity** disabilita Advanced Data Security in un server.</span><span class="sxs-lookup"><span data-stu-id="fdc4b-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="fdc4b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdc4b-107">EXAMPLES</span></span>

### <span data-ttu-id="fdc4b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fdc4b-108">Example 1</span></span>
### <span data-ttu-id="fdc4b-109">Esempio 2: Disabilitare Advanced Data Security del server</span><span class="sxs-lookup"><span data-stu-id="fdc4b-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="fdc4b-110">Esempio 3: Disabilitare Advanced Data Security del server dalla risorsa server</span><span class="sxs-lookup"><span data-stu-id="fdc4b-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="fdc4b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdc4b-111">PARAMETERS</span></span>

### <span data-ttu-id="fdc4b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc4b-112">-DefaultProfile</span></span>
<span data-ttu-id="fdc4b-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdc4b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdc4b-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdc4b-114">-InputObject</span></span>
<span data-ttu-id="fdc4b-115">Oggetto server da usare con l'operazione dei criteri di Sicurezza dei dati avanzata</span><span class="sxs-lookup"><span data-stu-id="fdc4b-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="fdc4b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdc4b-116">-ResourceGroupName</span></span>
<span data-ttu-id="fdc4b-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fdc4b-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="fdc4b-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fdc4b-118">-ServerName</span></span>
<span data-ttu-id="fdc4b-119">SQL del server di database.</span><span class="sxs-lookup"><span data-stu-id="fdc4b-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="fdc4b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdc4b-120">-Confirm</span></span>
<span data-ttu-id="fdc4b-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdc4b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdc4b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdc4b-122">-WhatIf</span></span>
<span data-ttu-id="fdc4b-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdc4b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdc4b-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdc4b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdc4b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc4b-125">CommonParameters</span></span>
<span data-ttu-id="fdc4b-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdc4b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc4b-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fdc4b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc4b-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="fdc4b-128">INPUTS</span></span>

### <span data-ttu-id="fdc4b-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="fdc4b-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="fdc4b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fdc4b-130">System.String</span></span>

## <span data-ttu-id="fdc4b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdc4b-131">OUTPUTS</span></span>

### <span data-ttu-id="fdc4b-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fdc4b-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="fdc4b-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="fdc4b-133">NOTES</span></span>

## <span data-ttu-id="fdc4b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdc4b-134">RELATED LINKS</span></span>
