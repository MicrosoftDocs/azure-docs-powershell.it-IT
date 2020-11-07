---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: c2c3b634eb5a9e031c375a6cc696298becd58e8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856701"
---
# <span data-ttu-id="dad8d-101">Enable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="dad8d-101">Enable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="dad8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dad8d-102">SYNOPSIS</span></span>
<span data-ttu-id="dad8d-103">Abilita la sicurezza avanzata dei dati in un server.</span><span class="sxs-lookup"><span data-stu-id="dad8d-103">Enables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="dad8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dad8d-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dad8d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dad8d-105">DESCRIPTION</span></span>
<span data-ttu-id="dad8d-106">Il cmdlet **Enable-AzSqlServerAdvancedDataSecurity** Abilita la sicurezza avanzata dei dati in un server.</span><span class="sxs-lookup"><span data-stu-id="dad8d-106">The **Enable-AzSqlServerAdvancedDataSecurity** cmdlet enables Advanced Data Security on a server.</span></span> <span data-ttu-id="dad8d-107">Advanced Data Security è un pacchetto di sicurezza unificato che include la classificazione dei dati, la valutazione delle vulnerabilità e la protezione avanzata delle minacce per il server.</span><span class="sxs-lookup"><span data-stu-id="dad8d-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your server.</span></span> <span data-ttu-id="dad8d-108">Verrà creato automaticamente un nuovo account di archiviazione per il salvataggio delle valutazioni della vulnerabilità.</span><span class="sxs-lookup"><span data-stu-id="dad8d-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="dad8d-109">Se un account di archiviazione è stato creato in precedenza per questo scopo, verrà usato al suo posto)</span><span class="sxs-lookup"><span data-stu-id="dad8d-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="dad8d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dad8d-110">EXAMPLES</span></span>

### <span data-ttu-id="dad8d-111">Esempio 1-abilitare la sicurezza dei dati avanzata del server</span><span class="sxs-lookup"><span data-stu-id="dad8d-111">Example 1 - Enable server Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="dad8d-112">Esempio 2-abilitare il server Advanced Data Security da Resource Server</span><span class="sxs-lookup"><span data-stu-id="dad8d-112">Example 2 - Enable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="dad8d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dad8d-113">PARAMETERS</span></span>

### <span data-ttu-id="dad8d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dad8d-114">-AsJob</span></span>
<span data-ttu-id="dad8d-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dad8d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dad8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad8d-116">-DefaultProfile</span></span>
<span data-ttu-id="dad8d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dad8d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad8d-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="dad8d-118">-DeploymentName</span></span>
<span data-ttu-id="dad8d-119">Specificare un nome personalizzato per la distribuzione avanzata della sicurezza dei dati</span><span class="sxs-lookup"><span data-stu-id="dad8d-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="dad8d-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="dad8d-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="dad8d-121">Non abilitare automaticamente la valutazione della vulnerabilità (non verrà creato un account di archiviazione)</span><span class="sxs-lookup"><span data-stu-id="dad8d-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="dad8d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dad8d-122">-InputObject</span></span>
<span data-ttu-id="dad8d-123">L'oggetto server da usare con l'operazione Advanced Data Security Policy</span><span class="sxs-lookup"><span data-stu-id="dad8d-123">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="dad8d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad8d-124">-ResourceGroupName</span></span>
<span data-ttu-id="dad8d-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dad8d-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="dad8d-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="dad8d-126">-ServerName</span></span>
<span data-ttu-id="dad8d-127">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="dad8d-127">SQL Database server name.</span></span>

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

### <span data-ttu-id="dad8d-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dad8d-128">-Confirm</span></span>
<span data-ttu-id="dad8d-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dad8d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad8d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad8d-130">-WhatIf</span></span>
<span data-ttu-id="dad8d-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dad8d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dad8d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dad8d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad8d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad8d-133">CommonParameters</span></span>
<span data-ttu-id="dad8d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad8d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad8d-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad8d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad8d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dad8d-136">INPUTS</span></span>

### <span data-ttu-id="dad8d-137">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="dad8d-137">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="dad8d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dad8d-138">System.String</span></span>

## <span data-ttu-id="dad8d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dad8d-139">OUTPUTS</span></span>

### <span data-ttu-id="dad8d-140">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="dad8d-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="dad8d-141">Note</span><span class="sxs-lookup"><span data-stu-id="dad8d-141">NOTES</span></span>

## <span data-ttu-id="dad8d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dad8d-142">RELATED LINKS</span></span>
