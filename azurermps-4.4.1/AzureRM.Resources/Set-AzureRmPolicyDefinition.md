---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 2404c0f2dc6c357503f23e7ed509f1c58c352c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687698"
---
# <span data-ttu-id="d1696-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d1696-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="d1696-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1696-102">SYNOPSIS</span></span>
<span data-ttu-id="d1696-103">Modifica la definizione di un criterio.</span><span class="sxs-lookup"><span data-stu-id="d1696-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1696-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1696-104">SYNTAX</span></span>

### <span data-ttu-id="d1696-105">Set di parametri nome definizione criteri.</span><span class="sxs-lookup"><span data-stu-id="d1696-105">The policy definition name parameter set.</span></span> <span data-ttu-id="d1696-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="d1696-106">(Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d1696-107">Set di parametri ID definizione criteri.</span><span class="sxs-lookup"><span data-stu-id="d1696-107">The policy definition Id parameter set.</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d1696-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1696-108">DESCRIPTION</span></span>
<span data-ttu-id="d1696-109">Il cmdlet **set-AzureRmPolicyDefinition** modifica una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d1696-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="d1696-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1696-110">EXAMPLES</span></span>

### <span data-ttu-id="d1696-111">Esempio 1: aggiornare la descrizione di una definizione di criterio</span><span class="sxs-lookup"><span data-stu-id="d1696-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="d1696-112">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d1696-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="d1696-113">Il comando Archivia l'oggetto nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d1696-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="d1696-114">Il secondo comando Aggiorna la descrizione della definizione di criterio identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d1696-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="d1696-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1696-115">PARAMETERS</span></span>

### <span data-ttu-id="d1696-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d1696-116">-ApiVersion</span></span>
<span data-ttu-id="d1696-117">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d1696-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d1696-118">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="d1696-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d1696-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1696-119">-Description</span></span>
<span data-ttu-id="d1696-120">Specifica una nuova descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d1696-120">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="d1696-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d1696-121">-DisplayName</span></span>
<span data-ttu-id="d1696-122">Specifica un nuovo nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d1696-122">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="d1696-123">-ID</span><span class="sxs-lookup"><span data-stu-id="d1696-123">-Id</span></span>
<span data-ttu-id="d1696-124">Specifica l'ID di risorsa completo per la definizione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="d1696-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1696-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d1696-125">-InformationAction</span></span>
<span data-ttu-id="d1696-126">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d1696-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d1696-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1696-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1696-128">Continuare</span><span class="sxs-lookup"><span data-stu-id="d1696-128">Continue</span></span>
- <span data-ttu-id="d1696-129">Ignora</span><span class="sxs-lookup"><span data-stu-id="d1696-129">Ignore</span></span>
- <span data-ttu-id="d1696-130">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d1696-130">Inquire</span></span>
- <span data-ttu-id="d1696-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d1696-131">SilentlyContinue</span></span>
- <span data-ttu-id="d1696-132">Stop</span><span class="sxs-lookup"><span data-stu-id="d1696-132">Stop</span></span>
- <span data-ttu-id="d1696-133">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d1696-133">Suspend</span></span>

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

### <span data-ttu-id="d1696-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d1696-134">-InformationVariable</span></span>
<span data-ttu-id="d1696-135">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d1696-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d1696-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1696-136">-Name</span></span>
<span data-ttu-id="d1696-137">Specifica il nome della definizione di criterio che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="d1696-137">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1696-138">-Policy</span><span class="sxs-lookup"><span data-stu-id="d1696-138">-Policy</span></span>
<span data-ttu-id="d1696-139">Specifica la nuova regola dei criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d1696-139">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="d1696-140">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="d1696-140">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="d1696-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="d1696-141">-Pre</span></span>
<span data-ttu-id="d1696-142">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d1696-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d1696-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1696-143">-DefaultProfile</span></span>
<span data-ttu-id="d1696-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1696-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1696-145">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d1696-145">-Metadata</span></span>
<span data-ttu-id="d1696-146">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d1696-146">The metadata for policy definition.</span></span> <span data-ttu-id="d1696-147">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="d1696-147">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="d1696-148">Parametro-</span><span class="sxs-lookup"><span data-stu-id="d1696-148">-Parameter</span></span>
<span data-ttu-id="d1696-149">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d1696-149">The parameters declaration for policy definition.</span></span> <span data-ttu-id="d1696-150">Può trattarsi di un percorso di un nome file o di un URI che contiene la dichiarazione parameters o della dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="d1696-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="d1696-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1696-151">CommonParameters</span></span>
<span data-ttu-id="d1696-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1696-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1696-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1696-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1696-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1696-154">INPUTS</span></span>

## <span data-ttu-id="d1696-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1696-155">OUTPUTS</span></span>

### <span data-ttu-id="d1696-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d1696-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d1696-157">Note</span><span class="sxs-lookup"><span data-stu-id="d1696-157">NOTES</span></span>

## <span data-ttu-id="d1696-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1696-158">RELATED LINKS</span></span>

[<span data-ttu-id="d1696-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d1696-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d1696-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d1696-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d1696-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d1696-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


