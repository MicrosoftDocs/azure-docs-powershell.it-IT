---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: 15c052eedb0174b71581a390610274e10379035a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350923"
---
# <span data-ttu-id="fca64-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="fca64-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="fca64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fca64-102">SYNOPSIS</span></span>
<span data-ttu-id="fca64-103">Verifica che il nome del cluster sia valido e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="fca64-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="fca64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fca64-104">SYNTAX</span></span>

### <span data-ttu-id="fca64-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fca64-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fca64-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fca64-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fca64-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fca64-107">DESCRIPTION</span></span>
<span data-ttu-id="fca64-108">Verifica che il nome del cluster sia valido e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="fca64-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="fca64-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fca64-109">EXAMPLES</span></span>

### <span data-ttu-id="fca64-110">Esempio 1: verificare la disponibilità di un nome di cluster kusto in uso</span><span class="sxs-lookup"><span data-stu-id="fca64-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="fca64-111">Il comando sopra riportato restituisce se esiste un cluster kusto denominato "testnewkustocluster" nell'area "est US".</span><span class="sxs-lookup"><span data-stu-id="fca64-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="fca64-112">Esempio 2: verificare la disponibilità di un nome di cluster kusto non in uso</span><span class="sxs-lookup"><span data-stu-id="fca64-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="fca64-113">Il comando sopra riportato restituisce se esiste un cluster kusto denominato "availablekustocluster" nell'area "est US".</span><span class="sxs-lookup"><span data-stu-id="fca64-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="fca64-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fca64-114">PARAMETERS</span></span>

### <span data-ttu-id="fca64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca64-115">-DefaultProfile</span></span>
<span data-ttu-id="fca64-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fca64-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca64-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fca64-117">-InputObject</span></span>
<span data-ttu-id="fca64-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fca64-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fca64-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fca64-119">-Location</span></span>
<span data-ttu-id="fca64-120">Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fca64-120">Azure location.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca64-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fca64-121">-Name</span></span>
<span data-ttu-id="fca64-122">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="fca64-122">Cluster name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca64-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fca64-123">-SubscriptionId</span></span>
<span data-ttu-id="fca64-124">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fca64-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fca64-125">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="fca64-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca64-126">-Digitare</span><span class="sxs-lookup"><span data-stu-id="fca64-126">-Type</span></span>
<span data-ttu-id="fca64-127">Tipo di risorsa, Microsoft. kusto/cluster.</span><span class="sxs-lookup"><span data-stu-id="fca64-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca64-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fca64-128">-Confirm</span></span>
<span data-ttu-id="fca64-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fca64-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca64-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca64-130">-WhatIf</span></span>
<span data-ttu-id="fca64-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fca64-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fca64-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fca64-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca64-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca64-133">CommonParameters</span></span>
<span data-ttu-id="fca64-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fca64-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca64-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fca64-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca64-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fca64-136">INPUTS</span></span>

### <span data-ttu-id="fca64-137">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="fca64-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="fca64-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fca64-138">OUTPUTS</span></span>

### <span data-ttu-id="fca64-139">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="fca64-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="fca64-140">Note</span><span class="sxs-lookup"><span data-stu-id="fca64-140">NOTES</span></span>

<span data-ttu-id="fca64-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fca64-141">ALIASES</span></span>

<span data-ttu-id="fca64-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fca64-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fca64-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="fca64-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fca64-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fca64-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fca64-145">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="fca64-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fca64-146">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="fca64-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="fca64-147">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="fca64-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="fca64-148">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="fca64-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="fca64-149">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="fca64-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="fca64-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="fca64-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fca64-151">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fca64-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="fca64-152">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="fca64-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="fca64-153">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="fca64-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="fca64-154">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fca64-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fca64-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="fca64-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fca64-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fca64-156">RELATED LINKS</span></span>

