---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 9776f4a569c2b8ac47d3bc8e478ce9fbfaccab01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191054"
---
# <span data-ttu-id="14742-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="14742-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="14742-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14742-102">SYNOPSIS</span></span>
<span data-ttu-id="14742-103">Recupera i criteri di Sicurezza avanzata dei dati di un server.</span><span class="sxs-lookup"><span data-stu-id="14742-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="14742-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14742-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14742-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14742-105">DESCRIPTION</span></span>
<span data-ttu-id="14742-106">Il cmdlet **Get-AzSqlServerAdvancedDataSecurityPolicy** recupera i criteri di Advanced Data Security di un server.</span><span class="sxs-lookup"><span data-stu-id="14742-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="14742-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14742-107">EXAMPLES</span></span>

### <span data-ttu-id="14742-108">Esempio 1: ottiene advanced data security del server</span><span class="sxs-lookup"><span data-stu-id="14742-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="14742-109">Esempio 2: ottiene la sicurezza avanzata dei dati del server dalla risorsa server</span><span class="sxs-lookup"><span data-stu-id="14742-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="14742-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14742-110">PARAMETERS</span></span>

### <span data-ttu-id="14742-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14742-111">-DefaultProfile</span></span>
<span data-ttu-id="14742-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14742-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14742-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14742-113">-InputObject</span></span>
<span data-ttu-id="14742-114">Oggetto server da usare con l'operazione dei criteri di Sicurezza dei dati avanzata</span><span class="sxs-lookup"><span data-stu-id="14742-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="14742-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14742-115">-ResourceGroupName</span></span>
<span data-ttu-id="14742-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14742-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="14742-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="14742-117">-ServerName</span></span>
<span data-ttu-id="14742-118">SQL del server di database.</span><span class="sxs-lookup"><span data-stu-id="14742-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="14742-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14742-119">CommonParameters</span></span>
<span data-ttu-id="14742-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14742-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14742-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14742-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14742-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="14742-122">INPUTS</span></span>

### <span data-ttu-id="14742-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="14742-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="14742-124">System.String</span><span class="sxs-lookup"><span data-stu-id="14742-124">System.String</span></span>

## <span data-ttu-id="14742-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14742-125">OUTPUTS</span></span>

### <span data-ttu-id="14742-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="14742-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="14742-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="14742-127">NOTES</span></span>

## <span data-ttu-id="14742-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14742-128">RELATED LINKS</span></span>
