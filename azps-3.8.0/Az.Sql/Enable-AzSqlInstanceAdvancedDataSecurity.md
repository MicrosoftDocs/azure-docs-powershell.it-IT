---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 981baf0b0cd4d3ca70d18ab43b08bb2a16f7708f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865072"
---
# <span data-ttu-id="4e67e-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="4e67e-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="4e67e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e67e-102">SYNOPSIS</span></span>
<span data-ttu-id="4e67e-103">Abilita la sicurezza dei dati avanzata in un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="4e67e-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="4e67e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e67e-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e67e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e67e-105">DESCRIPTION</span></span>
<span data-ttu-id="4e67e-106">Il cmdlet **Enable-AzSqlInstanceAdvancedDataSecurity** Abilita la sicurezza dei dati avanzata in un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="4e67e-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="4e67e-107">Advanced Data Security è un pacchetto di sicurezza unificato che include la classificazione dei dati, la valutazione delle vulnerabilità e la protezione avanzata delle minacce per l'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="4e67e-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="4e67e-108">Verrà creato automaticamente un nuovo account di archiviazione per il salvataggio delle valutazioni della vulnerabilità.</span><span class="sxs-lookup"><span data-stu-id="4e67e-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="4e67e-109">Se un account di archiviazione è stato creato in precedenza per questo scopo, verrà usato al suo posto)</span><span class="sxs-lookup"><span data-stu-id="4e67e-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="4e67e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e67e-110">EXAMPLES</span></span>

### <span data-ttu-id="4e67e-111">Esempio 1-abilitare la sicurezza dei dati avanzata dell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="4e67e-111">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="4e67e-112">Esempio 2-abilitare la sicurezza dei dati avanzata dell'istanza gestita da una risorsa del server</span><span class="sxs-lookup"><span data-stu-id="4e67e-112">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="4e67e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e67e-113">PARAMETERS</span></span>

### <span data-ttu-id="4e67e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e67e-114">-AsJob</span></span>
<span data-ttu-id="4e67e-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4e67e-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e67e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e67e-116">-DefaultProfile</span></span>
<span data-ttu-id="4e67e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e67e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e67e-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="4e67e-118">-DeploymentName</span></span>
<span data-ttu-id="4e67e-119">Specificare un nome personalizzato per la distribuzione avanzata della sicurezza dei dati</span><span class="sxs-lookup"><span data-stu-id="4e67e-119">Supply a custom name for Advanced Data Security deployment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e67e-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="4e67e-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="4e67e-121">Non abilitare automaticamente la valutazione della vulnerabilità (non verrà creato un account di archiviazione)</span><span class="sxs-lookup"><span data-stu-id="4e67e-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e67e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e67e-122">-InputObject</span></span>
<span data-ttu-id="4e67e-123">L'oggetto istanza gestita da usare con l'operazione Advanced Data Security Policy</span><span class="sxs-lookup"><span data-stu-id="4e67e-123">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="4e67e-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4e67e-124">-InstanceName</span></span>
<span data-ttu-id="4e67e-125">Nome dell'istanza gestita del database SQL.</span><span class="sxs-lookup"><span data-stu-id="4e67e-125">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="4e67e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e67e-126">-ResourceGroupName</span></span>
<span data-ttu-id="4e67e-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e67e-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e67e-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e67e-128">-Confirm</span></span>
<span data-ttu-id="4e67e-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e67e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e67e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e67e-130">-WhatIf</span></span>
<span data-ttu-id="4e67e-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e67e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e67e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e67e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e67e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e67e-133">CommonParameters</span></span>
<span data-ttu-id="4e67e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e67e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e67e-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e67e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e67e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e67e-136">INPUTS</span></span>

### <span data-ttu-id="4e67e-137">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4e67e-137">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="4e67e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4e67e-138">System.String</span></span>

## <span data-ttu-id="4e67e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e67e-139">OUTPUTS</span></span>

### <span data-ttu-id="4e67e-140">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4e67e-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="4e67e-141">Note</span><span class="sxs-lookup"><span data-stu-id="4e67e-141">NOTES</span></span>

## <span data-ttu-id="4e67e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e67e-142">RELATED LINKS</span></span>
