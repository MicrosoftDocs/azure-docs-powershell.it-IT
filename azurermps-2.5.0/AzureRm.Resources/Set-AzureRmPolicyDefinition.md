---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: aa6687efb331cbb702ea36c53cc02cd77cefd45d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866004"
---
# <span data-ttu-id="2b186-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2b186-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="2b186-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b186-102">SYNOPSIS</span></span>
<span data-ttu-id="2b186-103">Modifica la definizione di un criterio.</span><span class="sxs-lookup"><span data-stu-id="2b186-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b186-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b186-104">SYNTAX</span></span>

### <span data-ttu-id="2b186-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b186-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2b186-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b186-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2b186-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b186-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2b186-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b186-108">IdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2b186-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b186-109">DESCRIPTION</span></span>
<span data-ttu-id="2b186-110">Il cmdlet **set-AzureRmPolicyDefinition** modifica una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="2b186-110">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="2b186-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b186-111">EXAMPLES</span></span>

### <span data-ttu-id="2b186-112">Esempio 1: aggiornare la descrizione di una definizione di criterio</span><span class="sxs-lookup"><span data-stu-id="2b186-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="2b186-113">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="2b186-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="2b186-114">Il comando Archivia l'oggetto nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="2b186-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="2b186-115">Il secondo comando Aggiorna la descrizione della definizione di criterio identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="2b186-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="2b186-116">Esempio 2: aggiornare la modalità di una definizione di criteri</span><span class="sxs-lookup"><span data-stu-id="2b186-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="2b186-117">Questo comando Aggiorna la definizione dei criteri denominata VMPolicyDefinition usando il cmdlet Set-AzureRmPolicyDefinition per impostare la proprietà Mode su "tutti".</span><span class="sxs-lookup"><span data-stu-id="2b186-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzureRmPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="2b186-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b186-118">PARAMETERS</span></span>

### <span data-ttu-id="2b186-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2b186-119">-ApiVersion</span></span>
<span data-ttu-id="2b186-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="2b186-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2b186-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="2b186-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2b186-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b186-122">-DefaultProfile</span></span>
<span data-ttu-id="2b186-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2b186-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b186-124">-Description</span></span>
<span data-ttu-id="2b186-125">Specifica una nuova descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2b186-125">Specifies a new description for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2b186-126">-DisplayName</span></span>
<span data-ttu-id="2b186-127">Specifica un nuovo nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2b186-127">Specifies a new display name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-128">-ID</span><span class="sxs-lookup"><span data-stu-id="2b186-128">-Id</span></span>
<span data-ttu-id="2b186-129">Specifica l'ID di risorsa completo per la definizione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="2b186-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2b186-130">-InformationAction</span></span>
<span data-ttu-id="2b186-131">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="2b186-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="2b186-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b186-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b186-133">Continuare</span><span class="sxs-lookup"><span data-stu-id="2b186-133">Continue</span></span>
- <span data-ttu-id="2b186-134">Ignora</span><span class="sxs-lookup"><span data-stu-id="2b186-134">Ignore</span></span>
- <span data-ttu-id="2b186-135">Informarsi</span><span class="sxs-lookup"><span data-stu-id="2b186-135">Inquire</span></span>
- <span data-ttu-id="2b186-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2b186-136">SilentlyContinue</span></span>
- <span data-ttu-id="2b186-137">Stop</span><span class="sxs-lookup"><span data-stu-id="2b186-137">Stop</span></span>
- <span data-ttu-id="2b186-138">Sospensione</span><span class="sxs-lookup"><span data-stu-id="2b186-138">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2b186-139">-InformationVariable</span></span>
<span data-ttu-id="2b186-140">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="2b186-140">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="2b186-141">-ManagementGroupName</span></span>
<span data-ttu-id="2b186-142">Nome del gruppo di gestione della definizione di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="2b186-142">The name of the management group of the policy definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="2b186-143">-Metadata</span></span>
<span data-ttu-id="2b186-144">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2b186-144">The metadata for policy definition.</span></span> <span data-ttu-id="2b186-145">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="2b186-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-146">-Modalità</span><span class="sxs-lookup"><span data-stu-id="2b186-146">-Mode</span></span>
<span data-ttu-id="2b186-147">Modalità della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="2b186-147">The mode of the new policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b186-148">-Name</span></span>
<span data-ttu-id="2b186-149">Specifica il nome della definizione di criterio che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="2b186-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-150">Parametro-</span><span class="sxs-lookup"><span data-stu-id="2b186-150">-Parameter</span></span>
<span data-ttu-id="2b186-151">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2b186-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="2b186-152">Può trattarsi di un percorso di un nome file o di un URI che contiene la dichiarazione parameters o della dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="2b186-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-153">-Policy</span><span class="sxs-lookup"><span data-stu-id="2b186-153">-Policy</span></span>
<span data-ttu-id="2b186-154">Specifica la nuova regola dei criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2b186-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="2b186-155">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="2b186-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="2b186-156">-Pre</span></span>
<span data-ttu-id="2b186-157">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="2b186-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2b186-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b186-158">-SubscriptionId</span></span>
<span data-ttu-id="2b186-159">ID sottoscrizione della definizione di criterio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="2b186-159">The subscription ID of the policy definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b186-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b186-160">CommonParameters</span></span>
<span data-ttu-id="2b186-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b186-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b186-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b186-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b186-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b186-163">INPUTS</span></span>

## <span data-ttu-id="2b186-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b186-164">OUTPUTS</span></span>

## <span data-ttu-id="2b186-165">Note</span><span class="sxs-lookup"><span data-stu-id="2b186-165">NOTES</span></span>

## <span data-ttu-id="2b186-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b186-166">RELATED LINKS</span></span>

[<span data-ttu-id="2b186-167">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2b186-167">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="2b186-168">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2b186-168">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="2b186-169">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2b186-169">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


