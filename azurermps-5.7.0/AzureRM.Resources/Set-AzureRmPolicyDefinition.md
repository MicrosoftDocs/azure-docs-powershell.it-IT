---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: d7e01294836145b09844fa3bca49421df20f67d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519864"
---
# <span data-ttu-id="fada5-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fada5-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="fada5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fada5-102">SYNOPSIS</span></span>
<span data-ttu-id="fada5-103">Modifica la definizione di un criterio.</span><span class="sxs-lookup"><span data-stu-id="fada5-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fada5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fada5-104">SYNTAX</span></span>

### <span data-ttu-id="fada5-105">SetByPolicyDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fada5-105">SetByPolicyDefinitionName (Default)</span></span>
```
Set-AzureRmPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fada5-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="fada5-106">GetByPolicyDefintionName</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fada5-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="fada5-107">GetByPolicyDefinitionId</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fada5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fada5-108">DESCRIPTION</span></span>
<span data-ttu-id="fada5-109">Il cmdlet **set-AzureRmPolicyDefinition** modifica una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="fada5-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="fada5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fada5-110">EXAMPLES</span></span>

### <span data-ttu-id="fada5-111">Esempio 1: aggiornare la descrizione di una definizione di criterio</span><span class="sxs-lookup"><span data-stu-id="fada5-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="fada5-112">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="fada5-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="fada5-113">Il comando Archivia l'oggetto nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="fada5-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="fada5-114">Il secondo comando Aggiorna la descrizione della definizione di criterio identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="fada5-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="fada5-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fada5-115">PARAMETERS</span></span>

### <span data-ttu-id="fada5-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fada5-116">-ApiVersion</span></span>
<span data-ttu-id="fada5-117">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="fada5-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fada5-118">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="fada5-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fada5-119">-DefaultProfile</span></span>
<span data-ttu-id="fada5-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fada5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="fada5-121">-Description</span></span>
<span data-ttu-id="fada5-122">Specifica una nuova descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fada5-122">Specifies a new description for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fada5-123">-DisplayName</span></span>
<span data-ttu-id="fada5-124">Specifica un nuovo nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fada5-124">Specifies a new display name for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-125">-ID</span><span class="sxs-lookup"><span data-stu-id="fada5-125">-Id</span></span>
<span data-ttu-id="fada5-126">Specifica l'ID di risorsa completo per la definizione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="fada5-126">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fada5-127">-InformationAction</span></span>
<span data-ttu-id="fada5-128">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="fada5-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fada5-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fada5-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fada5-130">Continuare</span><span class="sxs-lookup"><span data-stu-id="fada5-130">Continue</span></span>
- <span data-ttu-id="fada5-131">Ignora</span><span class="sxs-lookup"><span data-stu-id="fada5-131">Ignore</span></span>
- <span data-ttu-id="fada5-132">Informarsi</span><span class="sxs-lookup"><span data-stu-id="fada5-132">Inquire</span></span>
- <span data-ttu-id="fada5-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fada5-133">SilentlyContinue</span></span>
- <span data-ttu-id="fada5-134">Stop</span><span class="sxs-lookup"><span data-stu-id="fada5-134">Stop</span></span>
- <span data-ttu-id="fada5-135">Sospensione</span><span class="sxs-lookup"><span data-stu-id="fada5-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fada5-136">-InformationVariable</span></span>
<span data-ttu-id="fada5-137">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="fada5-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fada5-138">-Metadata</span></span>
<span data-ttu-id="fada5-139">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fada5-139">The metadata for policy definition.</span></span> <span data-ttu-id="fada5-140">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="fada5-140">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="fada5-141">-Name</span></span>
<span data-ttu-id="fada5-142">Specifica il nome della definizione di criterio che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="fada5-142">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-143">Parametro-</span><span class="sxs-lookup"><span data-stu-id="fada5-143">-Parameter</span></span>
<span data-ttu-id="fada5-144">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fada5-144">The parameters declaration for policy definition.</span></span> <span data-ttu-id="fada5-145">Può trattarsi di un percorso di un nome file o di un URI che contiene la dichiarazione parameters o della dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="fada5-145">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-146">-Policy</span><span class="sxs-lookup"><span data-stu-id="fada5-146">-Policy</span></span>
<span data-ttu-id="fada5-147">Specifica la nuova regola dei criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fada5-147">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="fada5-148">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="fada5-148">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="fada5-149">-Pre</span></span>
<span data-ttu-id="fada5-150">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="fada5-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fada5-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fada5-151">CommonParameters</span></span>
<span data-ttu-id="fada5-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fada5-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fada5-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fada5-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fada5-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fada5-154">INPUTS</span></span>

### <span data-ttu-id="fada5-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fada5-155">None</span></span>
<span data-ttu-id="fada5-156">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fada5-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fada5-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fada5-157">OUTPUTS</span></span>

### <span data-ttu-id="fada5-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fada5-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fada5-159">Note</span><span class="sxs-lookup"><span data-stu-id="fada5-159">NOTES</span></span>

## <span data-ttu-id="fada5-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fada5-160">RELATED LINKS</span></span>

[<span data-ttu-id="fada5-161">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fada5-161">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="fada5-162">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fada5-162">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="fada5-163">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fada5-163">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


