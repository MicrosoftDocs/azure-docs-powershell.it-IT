---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 5f4ee759fcfddf8e68bc41b68706ccaf2d582e96
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188801"
---
# <span data-ttu-id="54c46-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="54c46-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="54c46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54c46-102">SYNOPSIS</span></span>
<span data-ttu-id="54c46-103">Disabilita l'autenticazione di Azure AD solo per un'istanza specifica gestita da SQL.</span><span class="sxs-lookup"><span data-stu-id="54c46-103">Disables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="54c46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54c46-104">SYNTAX</span></span>

### <span data-ttu-id="54c46-105">UseResourceGroupAndInstanceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="54c46-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54c46-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54c46-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54c46-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54c46-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c46-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54c46-108">DESCRIPTION</span></span>
<span data-ttu-id="54c46-109">Il cmdlet **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication Disabilita** il requisito di autenticazione di Azure Active Directory (Azure ad) solo per un'istanza gestita di AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="54c46-109">The **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="54c46-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54c46-110">EXAMPLES</span></span>

### <span data-ttu-id="54c46-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="54c46-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="54c46-112">Questo comando Disabilita Azure Active Directory (Azure AD) solo il requisito di autenticazione per un'istanza gestita AzureSQL denominata ManagedInstance01 associata a un gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="54c46-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="54c46-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54c46-113">PARAMETERS</span></span>

### <span data-ttu-id="54c46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c46-114">-DefaultProfile</span></span>
<span data-ttu-id="54c46-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54c46-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c46-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54c46-116">-InputObject</span></span>
<span data-ttu-id="54c46-117">Oggetto istanza gestito da usare.</span><span class="sxs-lookup"><span data-stu-id="54c46-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="54c46-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="54c46-118">-InstanceName</span></span>
<span data-ttu-id="54c46-119">Nome dell'istanza gestita di Azure SQL in cui è attiva solo l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54c46-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="54c46-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c46-120">-ResourceGroupName</span></span>
<span data-ttu-id="54c46-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54c46-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="54c46-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54c46-122">-ResourceId</span></span>
<span data-ttu-id="54c46-123">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="54c46-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="54c46-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="54c46-124">-Confirm</span></span>
<span data-ttu-id="54c46-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c46-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c46-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c46-126">-WhatIf</span></span>
<span data-ttu-id="54c46-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54c46-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c46-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54c46-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c46-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c46-129">CommonParameters</span></span>
<span data-ttu-id="54c46-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c46-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c46-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54c46-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c46-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54c46-132">INPUTS</span></span>

### <span data-ttu-id="54c46-133">System. String</span><span class="sxs-lookup"><span data-stu-id="54c46-133">System.String</span></span>

## <span data-ttu-id="54c46-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54c46-134">OUTPUTS</span></span>

### <span data-ttu-id="54c46-135">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="54c46-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="54c46-136">Note</span><span class="sxs-lookup"><span data-stu-id="54c46-136">NOTES</span></span>

## <span data-ttu-id="54c46-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54c46-137">RELATED LINKS</span></span>

[<span data-ttu-id="54c46-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="54c46-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="54c46-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="54c46-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="54c46-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="54c46-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="54c46-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="54c46-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)