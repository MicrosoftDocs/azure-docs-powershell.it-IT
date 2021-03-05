---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: a52d1d44647d2b608a34a07722439f243ba08510
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008830"
---
# <span data-ttu-id="f1f5f-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f1f5f-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="f1f5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f5f-103">Crea un assembly di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="f1f5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1f5f-104">SYNTAX</span></span>

### <span data-ttu-id="f1f5f-105">ByIntegrationAccountAndFilePath (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f1f5f-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1f5f-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="f1f5f-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1f5f-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="f1f5f-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1f5f-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="f1f5f-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1f5f-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="f1f5f-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1f5f-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="f1f5f-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1f5f-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="f1f5f-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1f5f-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="f1f5f-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1f5f-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="f1f5f-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1f5f-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f1f5f-114">DESCRIPTION</span></span>
<span data-ttu-id="f1f5f-115">Il cmdlet **Get-AzIntegrationAccountAccountAccount Consente** di creare un nuovo assembly in un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="f1f5f-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1f5f-116">EXAMPLES</span></span>

### <span data-ttu-id="f1f5f-117">Esempio 1: Creare un nuovo assembly usando un file locale</span><span class="sxs-lookup"><span data-stu-id="f1f5f-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="f1f5f-118">Crea un nuovo assembly usando il file locale che si trova nel percorso del file contenuto in "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="f1f5f-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="f1f5f-119">Esempio 2: Creare un nuovo assembly usando dati di tipo byte</span><span class="sxs-lookup"><span data-stu-id="f1f5f-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="f1f5f-120">Crea un nuovo assembly usando la matrice di byte contenuta in "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="f1f5f-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="f1f5f-121">Esempio 3: Creare un nuovo assembly usando un collegamento di contenuto</span><span class="sxs-lookup"><span data-stu-id="f1f5f-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="f1f5f-122">Crea un nuovo assembly usando i dati di byte che si trovano nell'URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="f1f5f-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="f1f5f-123">Questo è il metodo suggerito per la creazione di assembly di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="f1f5f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1f5f-124">PARAMETERS</span></span>

### <span data-ttu-id="f1f5f-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="f1f5f-125">-AssemblyData</span></span>
<span data-ttu-id="f1f5f-126">Dati di byte di assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="f1f5f-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="f1f5f-127">-AssemblyFilePath</span></span>
<span data-ttu-id="f1f5f-128">Percorso file assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="f1f5f-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="f1f5f-129">-ContentLink</span></span>
<span data-ttu-id="f1f5f-130">Collegamento pubblico ai dati di assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="f1f5f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f5f-131">-DefaultProfile</span></span>
<span data-ttu-id="f1f5f-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f5f-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f1f5f-133">-Metadata</span></span>
<span data-ttu-id="f1f5f-134">Metadati dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="f1f5f-135">-Name</span><span class="sxs-lookup"><span data-stu-id="f1f5f-135">-Name</span></span>
<span data-ttu-id="f1f5f-136">Nome assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="f1f5f-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="f1f5f-137">-ParentName</span></span>
<span data-ttu-id="f1f5f-138">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-138">The integration account name.</span></span>

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

### <span data-ttu-id="f1f5f-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f1f5f-139">-ParentObject</span></span>
<span data-ttu-id="f1f5f-140">Oggetto account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-140">An integration account object.</span></span>

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

### <span data-ttu-id="f1f5f-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f1f5f-141">-ParentResourceId</span></span>
<span data-ttu-id="f1f5f-142">ID risorsa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="f1f5f-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f5f-143">-ResourceGroupName</span></span>
<span data-ttu-id="f1f5f-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-144">The resource group name.</span></span>

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

### <span data-ttu-id="f1f5f-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1f5f-145">-Confirm</span></span>
<span data-ttu-id="f1f5f-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1f5f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1f5f-147">-WhatIf</span></span>
<span data-ttu-id="f1f5f-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1f5f-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1f5f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f5f-150">CommonParameters</span></span>
<span data-ttu-id="f1f5f-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f5f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f5f-152">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f5f-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f5f-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="f1f5f-153">INPUTS</span></span>

### <span data-ttu-id="f1f5f-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="f1f5f-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="f1f5f-155">System.String</span><span class="sxs-lookup"><span data-stu-id="f1f5f-155">System.String</span></span>

## <span data-ttu-id="f1f5f-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1f5f-156">OUTPUTS</span></span>

### <span data-ttu-id="f1f5f-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAccount</span><span class="sxs-lookup"><span data-stu-id="f1f5f-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="f1f5f-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="f1f5f-158">NOTES</span></span>

## <span data-ttu-id="f1f5f-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1f5f-159">RELATED LINKS</span></span>
