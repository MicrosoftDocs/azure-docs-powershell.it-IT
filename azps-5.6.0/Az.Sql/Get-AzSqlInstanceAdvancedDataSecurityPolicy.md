---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 2d9fa7ef7d3763d2db1d963aa1b1cac41b711bd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014510"
---
# <span data-ttu-id="5127e-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="5127e-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="5127e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5127e-102">SYNOPSIS</span></span>
<span data-ttu-id="5127e-103">Recupera i criteri di Sicurezza avanzata dei dati di un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="5127e-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="5127e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5127e-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5127e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5127e-105">DESCRIPTION</span></span>
<span data-ttu-id="5127e-106">Il cmdlet **Get-AzSqlInstanceAdvancedDataSecurityPolicy** recupera i criteri di Advanced Data Security di un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="5127e-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="5127e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5127e-107">EXAMPLES</span></span>

### <span data-ttu-id="5127e-108">Esempio 1: ottiene l'istanza gestita Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="5127e-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="5127e-109">Esempio 2: ottiene l'istanza gestita Advanced Data Security dalla risorsa dell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="5127e-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="5127e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5127e-110">PARAMETERS</span></span>

### <span data-ttu-id="5127e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5127e-111">-DefaultProfile</span></span>
<span data-ttu-id="5127e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5127e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5127e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5127e-113">-InputObject</span></span>
<span data-ttu-id="5127e-114">Oggetto istanza gestita da usare con l'operazione dei criteri di Sicurezza avanzata dati</span><span class="sxs-lookup"><span data-stu-id="5127e-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5127e-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5127e-115">-InstanceName</span></span>
<span data-ttu-id="5127e-116">SQL di istanza gestita dal database.</span><span class="sxs-lookup"><span data-stu-id="5127e-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="5127e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5127e-117">-ResourceGroupName</span></span>
<span data-ttu-id="5127e-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5127e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="5127e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5127e-119">CommonParameters</span></span>
<span data-ttu-id="5127e-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5127e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5127e-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5127e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5127e-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="5127e-122">INPUTS</span></span>

### <span data-ttu-id="5127e-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="5127e-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="5127e-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5127e-124">System.String</span></span>

## <span data-ttu-id="5127e-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5127e-125">OUTPUTS</span></span>

### <span data-ttu-id="5127e-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5127e-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="5127e-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="5127e-127">NOTES</span></span>

## <span data-ttu-id="5127e-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5127e-128">RELATED LINKS</span></span>
