---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: fcb1283531b35365cc8c07016c839a1152011160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512992"
---
# <span data-ttu-id="f2c60-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f2c60-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="f2c60-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2c60-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c60-103">Modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f2c60-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2c60-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2c60-104">SYNTAX</span></span>

### <span data-ttu-id="f2c60-105">Set di parametri nome assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="f2c60-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="f2c60-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="f2c60-106">(Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f2c60-107">Set di parametri ID assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="f2c60-107">The policy assignment Id parameter set.</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f2c60-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2c60-108">DESCRIPTION</span></span>
<span data-ttu-id="f2c60-109">Il cmdlet **set-AzureRmPolicyAssignment** modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f2c60-109">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="f2c60-110">Specificare un'assegnazione in base all'ID o al nome e all'ambito.</span><span class="sxs-lookup"><span data-stu-id="f2c60-110">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="f2c60-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2c60-111">EXAMPLES</span></span>

### <span data-ttu-id="f2c60-112">Esempio 1: aggiornare il nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="f2c60-112">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="f2c60-113">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f2c60-113">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="f2c60-114">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f2c60-114">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="f2c60-115">Il secondo comando ottiene l'assegnazione di criteri denominata PolicyAssignment usando il cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="f2c60-115">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="f2c60-116">Il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="f2c60-116">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="f2c60-117">Il comando finale aggiorna il nome visualizzato nell'assegnazione di criteri identificata dalla proprietà **resourceId** di $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="f2c60-117">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="f2c60-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2c60-118">PARAMETERS</span></span>

### <span data-ttu-id="f2c60-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f2c60-119">-ApiVersion</span></span>
<span data-ttu-id="f2c60-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="f2c60-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f2c60-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="f2c60-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f2c60-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f2c60-122">-DisplayName</span></span>
<span data-ttu-id="f2c60-123">Specifica un nuovo nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f2c60-123">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="f2c60-124">-ID</span><span class="sxs-lookup"><span data-stu-id="f2c60-124">-Id</span></span>
<span data-ttu-id="f2c60-125">Specifica l'ID di risorsa completo per l'assegnazione di criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="f2c60-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c60-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f2c60-126">-InformationAction</span></span>
<span data-ttu-id="f2c60-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="f2c60-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f2c60-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2c60-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2c60-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="f2c60-129">Continue</span></span>
- <span data-ttu-id="f2c60-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="f2c60-130">Ignore</span></span>
- <span data-ttu-id="f2c60-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="f2c60-131">Inquire</span></span>
- <span data-ttu-id="f2c60-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f2c60-132">SilentlyContinue</span></span>
- <span data-ttu-id="f2c60-133">Stop</span><span class="sxs-lookup"><span data-stu-id="f2c60-133">Stop</span></span>
- <span data-ttu-id="f2c60-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="f2c60-134">Suspend</span></span>

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

### <span data-ttu-id="f2c60-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f2c60-135">-InformationVariable</span></span>
<span data-ttu-id="f2c60-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="f2c60-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f2c60-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2c60-137">-Name</span></span>
<span data-ttu-id="f2c60-138">Specifica il nome dell'assegnazione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="f2c60-138">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c60-139">-NotScope</span><span class="sxs-lookup"><span data-stu-id="f2c60-139">-NotScope</span></span>
<span data-ttu-id="f2c60-140">L'assegnazione dei criteri non è ambiti.</span><span class="sxs-lookup"><span data-stu-id="f2c60-140">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c60-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="f2c60-141">-Pre</span></span>
<span data-ttu-id="f2c60-142">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="f2c60-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f2c60-143">-Ambito</span><span class="sxs-lookup"><span data-stu-id="f2c60-143">-Scope</span></span>
<span data-ttu-id="f2c60-144">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="f2c60-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c60-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c60-145">-DefaultProfile</span></span>
<span data-ttu-id="f2c60-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2c60-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2c60-147">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2c60-147">-Description</span></span>
<span data-ttu-id="f2c60-148">Descrizione dell'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f2c60-148">The description for policy assignment.</span></span>

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

### <span data-ttu-id="f2c60-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="f2c60-149">-Sku</span></span>
<span data-ttu-id="f2c60-150">Tabella hash che rappresenta le proprietà SKU.</span><span class="sxs-lookup"><span data-stu-id="f2c60-150">A hash table which represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c60-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c60-151">CommonParameters</span></span>
<span data-ttu-id="f2c60-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2c60-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c60-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2c60-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c60-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2c60-154">INPUTS</span></span>

## <span data-ttu-id="f2c60-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2c60-155">OUTPUTS</span></span>

### <span data-ttu-id="f2c60-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f2c60-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f2c60-157">Note</span><span class="sxs-lookup"><span data-stu-id="f2c60-157">NOTES</span></span>

## <span data-ttu-id="f2c60-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2c60-158">RELATED LINKS</span></span>

[<span data-ttu-id="f2c60-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f2c60-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f2c60-160">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f2c60-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f2c60-161">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f2c60-161">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


