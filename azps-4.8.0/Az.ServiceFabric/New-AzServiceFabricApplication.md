---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 5295caae4ffa0138a1c81fd08a5614f6e636eb41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032187"
---
# <span data-ttu-id="b6eb8-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b6eb8-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="b6eb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="b6eb8-103">Creare un'applicazione nuova in tessuto del servizio in un gruppo di risorse e un cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="b6eb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6eb8-104">SYNTAX</span></span>

### <span data-ttu-id="b6eb8-105">SkipAppTypeVersion (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6eb8-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6eb8-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b6eb8-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6eb8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6eb8-107">DESCRIPTION</span></span>
<span data-ttu-id="b6eb8-108">Questo cmdlet crea una nuova applicazione di servizi in tessuto nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="b6eb8-109">Il parametro-PackageUrl può essere usato per creare la versione del tipo, se la versione del tipo si chiude già, ma in stato "non riuscito" il cmdlet chiederà se l'utente vuole ricreare la versione del tipo.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="b6eb8-110">Se continua nello stato "non riuscito", il comando interrompe il processo e genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="b6eb8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6eb8-111">EXAMPLES</span></span>

### <span data-ttu-id="b6eb8-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6eb8-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="b6eb8-113">Questo esempio crea l'applicazione "testApp" in gruppo risorse "testRG" e cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="b6eb8-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="b6eb8-114">Il tipo di applicazione "TestAppType" versione "V1" dovrebbe essere già presente nel cluster e i parametri dell'applicazione devono essere definiti nel manifesto dell'applicazione in caso contrario il cmdlet non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="b6eb8-115">Esempio 2: specifica-PackageUrl per creare la versione del tipo di applicazione prima di creare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="b6eb8-116">Questo esempio crea il tipo di applicazione "TestAppType" versione "V1" usando l'URL del pacchetto fornito.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="b6eb8-117">In seguito, continuerà il processo normale per creare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="b6eb8-118">Se la versione del tipo di applicazione viene già chiusa e lo stato di provisioning non è riuscito, verrà richiesto di decidere se l'utente vuole ricreare la versione del tipo.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="b6eb8-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6eb8-119">PARAMETERS</span></span>

### <span data-ttu-id="b6eb8-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="b6eb8-120">-ApplicationParameter</span></span>
<span data-ttu-id="b6eb8-121">Specificare i parametri dell'applicazione come coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="b6eb8-122">Questi parametri devono essere presenti nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="b6eb8-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="b6eb8-123">-ApplicationTypeName</span></span>
<span data-ttu-id="b6eb8-124">Specificare il nome del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="b6eb8-124">Specify the name of the application type</span></span>

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

### <span data-ttu-id="b6eb8-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b6eb8-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="b6eb8-126">Specificare la versione del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="b6eb8-126">Specify the application type version</span></span>

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

### <span data-ttu-id="b6eb8-127">-Clustername</span><span class="sxs-lookup"><span data-stu-id="b6eb8-127">-ClusterName</span></span>
<span data-ttu-id="b6eb8-128">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b6eb8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6eb8-129">-DefaultProfile</span></span>
<span data-ttu-id="b6eb8-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6eb8-131">-Force</span><span class="sxs-lookup"><span data-stu-id="b6eb8-131">-Force</span></span>
<span data-ttu-id="b6eb8-132">Continuare senza richieste</span><span class="sxs-lookup"><span data-stu-id="b6eb8-132">Continue without prompts</span></span>

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

### <span data-ttu-id="b6eb8-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="b6eb8-133">-MaximumNodeCount</span></span>
<span data-ttu-id="b6eb8-134">Specifica il numero massimo di nodi in cui inserire un'applicazione</span><span class="sxs-lookup"><span data-stu-id="b6eb8-134">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="b6eb8-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="b6eb8-135">-MinimumNodeCount</span></span>
<span data-ttu-id="b6eb8-136">Specifica il numero minimo di nodi in cui il tessuto di servizio riserva la capacità per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="b6eb8-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="b6eb8-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6eb8-137">-Name</span></span>
<span data-ttu-id="b6eb8-138">Specificare il nome dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b6eb8-138">Specify the name of the application</span></span>

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

### <span data-ttu-id="b6eb8-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="b6eb8-139">-PackageUrl</span></span>
<span data-ttu-id="b6eb8-140">Specificare l'URL del file di pacchetto dell'applicazione sfpkg</span><span class="sxs-lookup"><span data-stu-id="b6eb8-140">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="b6eb8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6eb8-141">-ResourceGroupName</span></span>
<span data-ttu-id="b6eb8-142">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b6eb8-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b6eb8-143">-Confirm</span></span>
<span data-ttu-id="b6eb8-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6eb8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6eb8-145">-WhatIf</span></span>
<span data-ttu-id="b6eb8-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6eb8-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6eb8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6eb8-148">CommonParameters</span></span>
<span data-ttu-id="b6eb8-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6eb8-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6eb8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6eb8-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6eb8-151">INPUTS</span></span>

### <span data-ttu-id="b6eb8-152">System. String</span><span class="sxs-lookup"><span data-stu-id="b6eb8-152">System.String</span></span>

### <span data-ttu-id="b6eb8-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6eb8-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b6eb8-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6eb8-154">OUTPUTS</span></span>

### <span data-ttu-id="b6eb8-155">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="b6eb8-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="b6eb8-156">Note</span><span class="sxs-lookup"><span data-stu-id="b6eb8-156">NOTES</span></span>

## <span data-ttu-id="b6eb8-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6eb8-157">RELATED LINKS</span></span>
