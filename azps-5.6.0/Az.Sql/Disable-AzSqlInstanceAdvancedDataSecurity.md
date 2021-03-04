---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 4116ddf22bb39ddfa78e07180aaf61da7e87bb7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982142"
---
# <span data-ttu-id="504c4-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="504c4-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="504c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="504c4-102">SYNOPSIS</span></span>
<span data-ttu-id="504c4-103">Disabilita Advanced Data Security in un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="504c4-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="504c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="504c4-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="504c4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="504c4-105">DESCRIPTION</span></span>
<span data-ttu-id="504c4-106">Il cmdlet **Disable-AzSqlInstanceAdvancedDataSecurity** disabilita Advanced Data Security per un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="504c4-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="504c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="504c4-107">EXAMPLES</span></span>

### <span data-ttu-id="504c4-108">Esempio 1 - Disabilitare Advanced Data Security per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="504c4-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="504c4-109">Esempio 2 - Disabilitare La sicurezza avanzata dei dati del server dalla risorsa dell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="504c4-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="504c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="504c4-110">PARAMETERS</span></span>

### <span data-ttu-id="504c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="504c4-111">-DefaultProfile</span></span>
<span data-ttu-id="504c4-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="504c4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="504c4-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="504c4-113">-InputObject</span></span>
<span data-ttu-id="504c4-114">Oggetto istanza gestita da usare con l'operazione dei criteri di Sicurezza avanzata dati</span><span class="sxs-lookup"><span data-stu-id="504c4-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="504c4-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="504c4-115">-InstanceName</span></span>
<span data-ttu-id="504c4-116">SQL di istanza gestita dal database.</span><span class="sxs-lookup"><span data-stu-id="504c4-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="504c4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="504c4-117">-ResourceGroupName</span></span>
<span data-ttu-id="504c4-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="504c4-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="504c4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="504c4-119">-Confirm</span></span>
<span data-ttu-id="504c4-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="504c4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="504c4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="504c4-121">-WhatIf</span></span>
<span data-ttu-id="504c4-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="504c4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="504c4-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="504c4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="504c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="504c4-124">CommonParameters</span></span>
<span data-ttu-id="504c4-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="504c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="504c4-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="504c4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="504c4-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="504c4-127">INPUTS</span></span>

### <span data-ttu-id="504c4-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="504c4-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="504c4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="504c4-129">System.String</span></span>

## <span data-ttu-id="504c4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="504c4-130">OUTPUTS</span></span>

### <span data-ttu-id="504c4-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="504c4-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="504c4-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="504c4-132">NOTES</span></span>

## <span data-ttu-id="504c4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="504c4-133">RELATED LINKS</span></span>
