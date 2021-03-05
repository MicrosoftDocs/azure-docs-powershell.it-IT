---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 013731d7c6ec414f14985dcc83cdf6cd7bf6e205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011485"
---
# <span data-ttu-id="caefe-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="caefe-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="caefe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caefe-102">SYNOPSIS</span></span>
<span data-ttu-id="caefe-103">Disabilita l'autenticazione di Azure AD solo per una SQL gestita specifica.</span><span class="sxs-lookup"><span data-stu-id="caefe-103">Disables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="caefe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="caefe-104">SYNTAX</span></span>

### <span data-ttu-id="caefe-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="caefe-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caefe-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="caefe-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caefe-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="caefe-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caefe-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="caefe-108">DESCRIPTION</span></span>
<span data-ttu-id="caefe-109">Il cmdlet **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** disabilita il requisito di autenticazione di Azure Active Directory (Azure AD) solo per un'istanza gestita di AzureSQL nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="caefe-109">The **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="caefe-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="caefe-110">EXAMPLES</span></span>

### <span data-ttu-id="caefe-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="caefe-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="caefe-112">Questo comando disabilita il requisito di autenticazione di Azure Active Directory (Azure AD) solo per un'istanza gestita di AzureSQL denominata ManagedInstance01 associata a un gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="caefe-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="caefe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="caefe-113">PARAMETERS</span></span>

### <span data-ttu-id="caefe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caefe-114">-DefaultProfile</span></span>
<span data-ttu-id="caefe-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="caefe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caefe-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="caefe-116">-InputObject</span></span>
<span data-ttu-id="caefe-117">L'oggetto istanza gestita da usare.</span><span class="sxs-lookup"><span data-stu-id="caefe-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caefe-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="caefe-118">-InstanceName</span></span>
<span data-ttu-id="caefe-119">Il nome dell'istanza SQL gestita di Azure in cui si trova solo l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="caefe-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caefe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caefe-120">-ResourceGroupName</span></span>
<span data-ttu-id="caefe-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="caefe-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caefe-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caefe-122">-ResourceId</span></span>
<span data-ttu-id="caefe-123">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="caefe-123">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caefe-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caefe-124">-Confirm</span></span>
<span data-ttu-id="caefe-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caefe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caefe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caefe-126">-WhatIf</span></span>
<span data-ttu-id="caefe-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="caefe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caefe-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="caefe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caefe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caefe-129">CommonParameters</span></span>
<span data-ttu-id="caefe-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caefe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caefe-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="caefe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caefe-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="caefe-132">INPUTS</span></span>

### <span data-ttu-id="caefe-133">System.String</span><span class="sxs-lookup"><span data-stu-id="caefe-133">System.String</span></span>

## <span data-ttu-id="caefe-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="caefe-134">OUTPUTS</span></span>

### <span data-ttu-id="caefe-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="caefe-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="caefe-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="caefe-136">NOTES</span></span>

## <span data-ttu-id="caefe-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="caefe-137">RELATED LINKS</span></span>

[<span data-ttu-id="caefe-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="caefe-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="caefe-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="caefe-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="caefe-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="caefe-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="caefe-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="caefe-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)