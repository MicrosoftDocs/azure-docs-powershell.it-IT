---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: e1e6efbdeaed90fe7591ed2dd5a645955dd5a314
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982158"
---
# <span data-ttu-id="379b5-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="379b5-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="379b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="379b5-102">SYNOPSIS</span></span>
<span data-ttu-id="379b5-103">Creare una nuova applicazione di tessuto di servizio nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="379b5-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="379b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="379b5-104">SYNTAX</span></span>

### <span data-ttu-id="379b5-105">SkipAppTypeVersion (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="379b5-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="379b5-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="379b5-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="379b5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="379b5-107">DESCRIPTION</span></span>
<span data-ttu-id="379b5-108">Questo cmdlet crea una nuova applicazione di tessuto di servizio nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="379b5-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="379b5-109">Il parametro -PackageUrl può essere usato per creare la versione del tipo, se la versione del tipo viene già chiusa ma nello stato "Non riuscito", il cmdlet chiederà se l'utente vuole ricreare la versione tipo.</span><span class="sxs-lookup"><span data-stu-id="379b5-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="379b5-110">Se continua con lo stato "Operazione non riuscita", il comando interrompe il processo e genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="379b5-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="379b5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="379b5-111">EXAMPLES</span></span>

### <span data-ttu-id="379b5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="379b5-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="379b5-113">Questo esempio crea l'applicazione "testApp" nel gruppo di risorse "testRG" e nel cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="379b5-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="379b5-114">Il tipo di applicazione "TestAppType" versione "v1" deve già esistere nel cluster e i parametri dell'applicazione devono essere definiti nel manifesto dell'applicazione, altrimenti il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="379b5-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="379b5-115">Esempio 2: Specificare -PackageUrl per creare la versione del tipo di applicazione prima di creare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="379b5-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="379b5-116">Questo esempio crea il tipo di applicazione "TestAppType" versione "v1" usando l'URL del pacchetto fornito.</span><span class="sxs-lookup"><span data-stu-id="379b5-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="379b5-117">Successivamente, continuerà il normale processo di creazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="379b5-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="379b5-118">Se la versione del tipo di applicazione viene già chiusa e lo stato di provisioning in "Non riuscita" viene chiesto di decidere se l'utente vuole ricreare la versione tipo.</span><span class="sxs-lookup"><span data-stu-id="379b5-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="379b5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="379b5-119">PARAMETERS</span></span>

### <span data-ttu-id="379b5-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="379b5-120">-ApplicationParameter</span></span>
<span data-ttu-id="379b5-121">Specificare i parametri dell'applicazione come coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="379b5-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="379b5-122">Questi parametri devono essere presenti nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="379b5-122">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="379b5-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="379b5-123">-ApplicationTypeName</span></span>
<span data-ttu-id="379b5-124">Specificare il nome del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="379b5-124">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379b5-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="379b5-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="379b5-126">Specificare la versione del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="379b5-126">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379b5-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="379b5-127">-ClusterName</span></span>
<span data-ttu-id="379b5-128">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="379b5-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="379b5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379b5-129">-DefaultProfile</span></span>
<span data-ttu-id="379b5-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="379b5-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="379b5-131">-Force</span><span class="sxs-lookup"><span data-stu-id="379b5-131">-Force</span></span>
<span data-ttu-id="379b5-132">Continuare senza chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="379b5-132">Continue without prompts</span></span>

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

### <span data-ttu-id="379b5-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="379b5-133">-MaximumNodeCount</span></span>
<span data-ttu-id="379b5-134">Specifica il numero massimo di nodi in cui inserire un'applicazione</span><span class="sxs-lookup"><span data-stu-id="379b5-134">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379b5-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="379b5-135">-MinimumNodeCount</span></span>
<span data-ttu-id="379b5-136">Specifica il numero minimo di nodi in cui Service Fabric riserva la capacità per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="379b5-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379b5-137">-Name</span><span class="sxs-lookup"><span data-stu-id="379b5-137">-Name</span></span>
<span data-ttu-id="379b5-138">Specificare il nome dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="379b5-138">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379b5-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="379b5-139">-PackageUrl</span></span>
<span data-ttu-id="379b5-140">Specificare l'URL del file sfpkg del pacchetto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="379b5-140">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAppTypeVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="379b5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379b5-141">-ResourceGroupName</span></span>
<span data-ttu-id="379b5-142">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="379b5-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="379b5-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="379b5-143">-Confirm</span></span>
<span data-ttu-id="379b5-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="379b5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="379b5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="379b5-145">-WhatIf</span></span>
<span data-ttu-id="379b5-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="379b5-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="379b5-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="379b5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="379b5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379b5-148">CommonParameters</span></span>
<span data-ttu-id="379b5-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="379b5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379b5-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="379b5-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379b5-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="379b5-151">INPUTS</span></span>

### <span data-ttu-id="379b5-152">System.String</span><span class="sxs-lookup"><span data-stu-id="379b5-152">System.String</span></span>

### <span data-ttu-id="379b5-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="379b5-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="379b5-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="379b5-154">OUTPUTS</span></span>

### <span data-ttu-id="379b5-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="379b5-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="379b5-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="379b5-156">NOTES</span></span>

## <span data-ttu-id="379b5-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="379b5-157">RELATED LINKS</span></span>
