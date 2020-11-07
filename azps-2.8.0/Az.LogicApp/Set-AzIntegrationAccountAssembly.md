---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: a3f2c76de9dc331c6b073f724fede6a3bafeed18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673972"
---
# <span data-ttu-id="5c1c9-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c1c9-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="5c1c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c1c9-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1c9-103">Modifica un assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="5c1c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c1c9-104">SYNTAX</span></span>

### <span data-ttu-id="5c1c9-105">ByIntegrationAccountAndFilePath (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c1c9-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1c9-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5c1c9-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c1c9-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5c1c9-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c1c9-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5c1c9-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1c9-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5c1c9-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1c9-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="5c1c9-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1c9-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="5c1c9-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1c9-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="5c1c9-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1c9-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="5c1c9-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c1c9-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c1c9-114">DESCRIPTION</span></span>
<span data-ttu-id="5c1c9-115">Il cmdlet **set-AzIntegrationAccountAssembly** modifica un assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="5c1c9-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c1c9-116">EXAMPLES</span></span>

### <span data-ttu-id="5c1c9-117">Esempio 1: modificare un assembly usando un file locale</span><span class="sxs-lookup"><span data-stu-id="5c1c9-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5c1c9-118">Modifica l'assembly denominato "sampleAssembly" usando il file locale che si trova nel percorso del file contenuto in "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="5c1c9-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="5c1c9-119">Esempio 2: modificare un assembly usando i dati di byte</span><span class="sxs-lookup"><span data-stu-id="5c1c9-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5c1c9-120">Modifica l'assembly denominato "sampleAssembly" usando la matrice di byte contenuta in "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="5c1c9-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="5c1c9-121">Esempio 3: modificare un assembly usando un collegamento contenuto</span><span class="sxs-lookup"><span data-stu-id="5c1c9-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="5c1c9-122">Modifica l'assembly denominato "sampleAssembly" usando i dati a byte presenti nell'URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="5c1c9-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="5c1c9-123">Questo è il metodo suggerito per la creazione di assembly di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="5c1c9-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c1c9-124">PARAMETERS</span></span>

### <span data-ttu-id="5c1c9-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="5c1c9-125">-AssemblyData</span></span>
<span data-ttu-id="5c1c9-126">Dati del byte dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="5c1c9-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="5c1c9-127">-AssemblyFilePath</span></span>
<span data-ttu-id="5c1c9-128">Percorso del file dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="5c1c9-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="5c1c9-129">-ContentLink</span></span>
<span data-ttu-id="5c1c9-130">Un collegamento accessibile pubblicamente ai dati dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="5c1c9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1c9-131">-DefaultProfile</span></span>
<span data-ttu-id="5c1c9-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c1c9-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c1c9-133">-InputObject</span></span>
<span data-ttu-id="5c1c9-134">Un assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1c9-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5c1c9-135">-Metadata</span></span>
<span data-ttu-id="5c1c9-136">Metadati dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="5c1c9-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c1c9-137">-Name</span></span>
<span data-ttu-id="5c1c9-138">Nome dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1c9-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="5c1c9-139">-ParentName</span></span>
<span data-ttu-id="5c1c9-140">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-140">The integration account name.</span></span>

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

### <span data-ttu-id="5c1c9-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1c9-141">-ResourceGroupName</span></span>
<span data-ttu-id="5c1c9-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-142">The resource group name.</span></span>

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

### <span data-ttu-id="5c1c9-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c1c9-143">-ResourceId</span></span>
<span data-ttu-id="5c1c9-144">ID risorsa dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="5c1c9-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5c1c9-145">-Confirm</span></span>
<span data-ttu-id="5c1c9-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c1c9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c1c9-147">-WhatIf</span></span>
<span data-ttu-id="5c1c9-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c1c9-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c1c9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1c9-150">CommonParameters</span></span>
<span data-ttu-id="5c1c9-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c1c9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1c9-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1c9-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1c9-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c1c9-153">INPUTS</span></span>

### <span data-ttu-id="5c1c9-154">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c1c9-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="5c1c9-155">System. String</span><span class="sxs-lookup"><span data-stu-id="5c1c9-155">System.String</span></span>

## <span data-ttu-id="5c1c9-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c1c9-156">OUTPUTS</span></span>

### <span data-ttu-id="5c1c9-157">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c1c9-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="5c1c9-158">Note</span><span class="sxs-lookup"><span data-stu-id="5c1c9-158">NOTES</span></span>

## <span data-ttu-id="5c1c9-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c1c9-159">RELATED LINKS</span></span>