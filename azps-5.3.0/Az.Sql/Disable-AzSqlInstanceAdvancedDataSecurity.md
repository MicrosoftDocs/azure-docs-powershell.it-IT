---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 39b23c1b39121f143791667ade542080ba70ec95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375325"
---
# <span data-ttu-id="3ad19-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="3ad19-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="3ad19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ad19-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad19-103">Disabilita la sicurezza dei dati avanzata in un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="3ad19-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="3ad19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ad19-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ad19-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ad19-105">DESCRIPTION</span></span>
<span data-ttu-id="3ad19-106">Il cmdlet **Disable-AzSqlInstanceAdvancedDataSecurity Disabilita** la sicurezza dei dati avanzata in un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="3ad19-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="3ad19-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ad19-107">EXAMPLES</span></span>

### <span data-ttu-id="3ad19-108">Esempio 1-disabilitare la sicurezza dei dati avanzata dell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="3ad19-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="3ad19-109">Esempio 2-disabilitare la sicurezza dei dati avanzata del server dalla risorsa istanza gestita</span><span class="sxs-lookup"><span data-stu-id="3ad19-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="3ad19-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ad19-110">PARAMETERS</span></span>

### <span data-ttu-id="3ad19-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad19-111">-DefaultProfile</span></span>
<span data-ttu-id="3ad19-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad19-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ad19-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ad19-113">-InputObject</span></span>
<span data-ttu-id="3ad19-114">L'oggetto istanza gestita da usare con l'operazione Advanced Data Security Policy</span><span class="sxs-lookup"><span data-stu-id="3ad19-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="3ad19-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3ad19-115">-InstanceName</span></span>
<span data-ttu-id="3ad19-116">Nome dell'istanza gestita del database SQL.</span><span class="sxs-lookup"><span data-stu-id="3ad19-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="3ad19-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad19-117">-ResourceGroupName</span></span>
<span data-ttu-id="3ad19-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ad19-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="3ad19-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ad19-119">-Confirm</span></span>
<span data-ttu-id="3ad19-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ad19-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ad19-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ad19-121">-WhatIf</span></span>
<span data-ttu-id="3ad19-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ad19-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ad19-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ad19-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ad19-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad19-124">CommonParameters</span></span>
<span data-ttu-id="3ad19-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad19-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad19-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ad19-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad19-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ad19-127">INPUTS</span></span>

### <span data-ttu-id="3ad19-128">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3ad19-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="3ad19-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3ad19-129">System.String</span></span>

## <span data-ttu-id="3ad19-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ad19-130">OUTPUTS</span></span>

### <span data-ttu-id="3ad19-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3ad19-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="3ad19-132">Note</span><span class="sxs-lookup"><span data-stu-id="3ad19-132">NOTES</span></span>

## <span data-ttu-id="3ad19-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ad19-133">RELATED LINKS</span></span>
