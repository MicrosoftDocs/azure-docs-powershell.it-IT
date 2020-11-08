---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022296"
---
# <span data-ttu-id="20fcd-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="20fcd-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="20fcd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="20fcd-103">Crea un assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20fcd-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="20fcd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20fcd-104">SYNTAX</span></span>

### <span data-ttu-id="20fcd-105">ByIntegrationAccountAndFilePath (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20fcd-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20fcd-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="20fcd-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20fcd-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="20fcd-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20fcd-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="20fcd-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20fcd-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="20fcd-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20fcd-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="20fcd-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20fcd-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="20fcd-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20fcd-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="20fcd-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20fcd-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="20fcd-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20fcd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20fcd-114">DESCRIPTION</span></span>
<span data-ttu-id="20fcd-115">Il cmdlet **Get-AzIntegrationAccountAssembly** crea un nuovo assembly in un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20fcd-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="20fcd-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20fcd-116">EXAMPLES</span></span>

### <span data-ttu-id="20fcd-117">Esempio 1: creare un nuovo assembly usando un file locale</span><span class="sxs-lookup"><span data-stu-id="20fcd-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="20fcd-118">Crea un nuovo assembly usando il file locale che si trova nel percorso del file contenuto in "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="20fcd-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="20fcd-119">Esempio 2: creare un nuovo assembly usando i dati di byte</span><span class="sxs-lookup"><span data-stu-id="20fcd-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="20fcd-120">Crea un nuovo assembly usando la matrice di byte contenuta in "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="20fcd-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="20fcd-121">Esempio 3: creare un nuovo assembly usando un collegamento contenuto</span><span class="sxs-lookup"><span data-stu-id="20fcd-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="20fcd-122">Crea un nuovo assembly usando i dati a byte presenti nell'URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="20fcd-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="20fcd-123">Questo è il metodo suggerito per la creazione di assembly di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="20fcd-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="20fcd-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20fcd-124">PARAMETERS</span></span>

### <span data-ttu-id="20fcd-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="20fcd-125">-AssemblyData</span></span>
<span data-ttu-id="20fcd-126">Dati del byte dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20fcd-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fcd-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="20fcd-127">-AssemblyFilePath</span></span>
<span data-ttu-id="20fcd-128">Percorso del file dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20fcd-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fcd-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="20fcd-129">-ContentLink</span></span>
<span data-ttu-id="20fcd-130">Un collegamento accessibile pubblicamente ai dati dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20fcd-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fcd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20fcd-131">-DefaultProfile</span></span>
<span data-ttu-id="20fcd-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20fcd-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20fcd-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="20fcd-133">-Metadata</span></span>
<span data-ttu-id="20fcd-134">Metadati dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20fcd-134">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fcd-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="20fcd-135">-Name</span></span>
<span data-ttu-id="20fcd-136">Nome dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20fcd-136">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fcd-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="20fcd-137">-ParentName</span></span>
<span data-ttu-id="20fcd-138">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20fcd-138">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fcd-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="20fcd-139">-ParentObject</span></span>
<span data-ttu-id="20fcd-140">Un oggetto account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20fcd-140">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20fcd-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="20fcd-141">-ParentResourceId</span></span>
<span data-ttu-id="20fcd-142">ID risorsa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="20fcd-142">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fcd-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20fcd-143">-ResourceGroupName</span></span>
<span data-ttu-id="20fcd-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="20fcd-144">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fcd-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="20fcd-145">-Confirm</span></span>
<span data-ttu-id="20fcd-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20fcd-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20fcd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20fcd-147">-WhatIf</span></span>
<span data-ttu-id="20fcd-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20fcd-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20fcd-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20fcd-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20fcd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20fcd-150">CommonParameters</span></span>
<span data-ttu-id="20fcd-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20fcd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20fcd-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20fcd-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20fcd-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20fcd-153">INPUTS</span></span>

### <span data-ttu-id="20fcd-154">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="20fcd-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="20fcd-155">System. String</span><span class="sxs-lookup"><span data-stu-id="20fcd-155">System.String</span></span>

## <span data-ttu-id="20fcd-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20fcd-156">OUTPUTS</span></span>

### <span data-ttu-id="20fcd-157">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="20fcd-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="20fcd-158">Note</span><span class="sxs-lookup"><span data-stu-id="20fcd-158">NOTES</span></span>

## <span data-ttu-id="20fcd-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20fcd-159">RELATED LINKS</span></span>
