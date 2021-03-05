---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 372951b708d34c44706f981424b7ace39efff2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974189"
---
# <span data-ttu-id="ca953-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="ca953-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="ca953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca953-102">SYNOPSIS</span></span>
<span data-ttu-id="ca953-103">Recupera i criteri di Sicurezza avanzata dei dati di un server.</span><span class="sxs-lookup"><span data-stu-id="ca953-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="ca953-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca953-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca953-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ca953-105">DESCRIPTION</span></span>
<span data-ttu-id="ca953-106">Il cmdlet **Get-AzSqlServerAdvancedDataSecurityPolicy** recupera i criteri di Advanced Data Security di un server.</span><span class="sxs-lookup"><span data-stu-id="ca953-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="ca953-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca953-107">EXAMPLES</span></span>

### <span data-ttu-id="ca953-108">Esempio 1: ottiene advanced data security del server</span><span class="sxs-lookup"><span data-stu-id="ca953-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="ca953-109">Esempio 2: ottiene la sicurezza avanzata dei dati del server dalla risorsa server</span><span class="sxs-lookup"><span data-stu-id="ca953-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="ca953-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca953-110">PARAMETERS</span></span>

### <span data-ttu-id="ca953-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca953-111">-DefaultProfile</span></span>
<span data-ttu-id="ca953-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca953-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca953-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca953-113">-InputObject</span></span>
<span data-ttu-id="ca953-114">Oggetto server da usare con l'operazione dei criteri di sicurezza dei dati avanzata</span><span class="sxs-lookup"><span data-stu-id="ca953-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="ca953-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca953-115">-ResourceGroupName</span></span>
<span data-ttu-id="ca953-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca953-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca953-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca953-117">-ServerName</span></span>
<span data-ttu-id="ca953-118">SQL del server di database.</span><span class="sxs-lookup"><span data-stu-id="ca953-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="ca953-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca953-119">CommonParameters</span></span>
<span data-ttu-id="ca953-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca953-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca953-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ca953-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca953-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="ca953-122">INPUTS</span></span>

### <span data-ttu-id="ca953-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="ca953-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="ca953-124">System.String</span><span class="sxs-lookup"><span data-stu-id="ca953-124">System.String</span></span>

## <span data-ttu-id="ca953-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca953-125">OUTPUTS</span></span>

### <span data-ttu-id="ca953-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ca953-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="ca953-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="ca953-127">NOTES</span></span>

## <span data-ttu-id="ca953-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca953-128">RELATED LINKS</span></span>
