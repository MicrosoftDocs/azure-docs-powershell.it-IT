---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200391"
---
# <span data-ttu-id="38fd4-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="38fd4-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="38fd4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="38fd4-103">Crea un nuovo valore denominato.</span><span class="sxs-lookup"><span data-stu-id="38fd4-103">Creates new Named Value.</span></span>

## <span data-ttu-id="38fd4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38fd4-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38fd4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38fd4-105">DESCRIPTION</span></span>
<span data-ttu-id="38fd4-106">Il cmdlet **New-AzApiManagementNamedValue** crea una gestione API di Azure **denominata value**.</span><span class="sxs-lookup"><span data-stu-id="38fd4-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="38fd4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38fd4-107">EXAMPLES</span></span>

### <span data-ttu-id="38fd4-108">Esempio 1: creare un valore denominato che include tag</span><span class="sxs-lookup"><span data-stu-id="38fd4-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="38fd4-109">Il primo comando assegna due valori alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="38fd4-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="38fd4-110">Il secondo comando crea un valore denominato e assegna le stringhe in $Tags come tag nella proprietà.</span><span class="sxs-lookup"><span data-stu-id="38fd4-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="38fd4-111">Esempio 2: creare un valore denominato con un valore segreto</span><span class="sxs-lookup"><span data-stu-id="38fd4-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="38fd4-112">Questo comando crea un **valore denominato** che contiene un valore crittografato.</span><span class="sxs-lookup"><span data-stu-id="38fd4-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="38fd4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38fd4-113">PARAMETERS</span></span>

### <span data-ttu-id="38fd4-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="38fd4-114">-Context</span></span>
<span data-ttu-id="38fd4-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="38fd4-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="38fd4-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="38fd4-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38fd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38fd4-117">-DefaultProfile</span></span>
<span data-ttu-id="38fd4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38fd4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38fd4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="38fd4-119">-Name</span></span>
<span data-ttu-id="38fd4-120">Nome del valore denominato.</span><span class="sxs-lookup"><span data-stu-id="38fd4-120">Name of the named value.</span></span>
<span data-ttu-id="38fd4-121">La lunghezza massima è di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="38fd4-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="38fd4-122">Può contenere solo lettere, cifre, punto, trattino e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="38fd4-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="38fd4-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="38fd4-123">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38fd4-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="38fd4-124">-NamedValueId</span></span>
<span data-ttu-id="38fd4-125">Identificatore del nuovo valore denominato.</span><span class="sxs-lookup"><span data-stu-id="38fd4-125">Identifier of new named value.</span></span>
<span data-ttu-id="38fd4-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="38fd4-126">This parameter is optional.</span></span>
<span data-ttu-id="38fd4-127">Se non viene specificato verrà generato.</span><span class="sxs-lookup"><span data-stu-id="38fd4-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="38fd4-128">-Segreto</span><span class="sxs-lookup"><span data-stu-id="38fd4-128">-Secret</span></span>
<span data-ttu-id="38fd4-129">Determina se il valore è un segreto e deve essere crittografato o meno.</span><span class="sxs-lookup"><span data-stu-id="38fd4-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="38fd4-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="38fd4-130">This parameter is optional.</span></span>
<span data-ttu-id="38fd4-131">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="38fd4-131">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38fd4-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="38fd4-132">-Tag</span></span>
<span data-ttu-id="38fd4-133">Tag da associare al valore denominato.</span><span class="sxs-lookup"><span data-stu-id="38fd4-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="38fd4-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="38fd4-134">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38fd4-135">-Valore</span><span class="sxs-lookup"><span data-stu-id="38fd4-135">-Value</span></span>
<span data-ttu-id="38fd4-136">Valore del valore denominato.</span><span class="sxs-lookup"><span data-stu-id="38fd4-136">Value of the named value.</span></span>
<span data-ttu-id="38fd4-137">Può contenere espressioni di criteri.</span><span class="sxs-lookup"><span data-stu-id="38fd4-137">Can contain policy expressions.</span></span>
<span data-ttu-id="38fd4-138">La lunghezza massima è di 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="38fd4-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="38fd4-139">Potrebbe non essere vuoto o costituito solo da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="38fd4-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="38fd4-140">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="38fd4-140">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38fd4-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38fd4-141">-Confirm</span></span>
<span data-ttu-id="38fd4-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38fd4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38fd4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38fd4-143">-WhatIf</span></span>
<span data-ttu-id="38fd4-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38fd4-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38fd4-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38fd4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38fd4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38fd4-146">CommonParameters</span></span>
<span data-ttu-id="38fd4-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38fd4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38fd4-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38fd4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38fd4-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38fd4-149">INPUTS</span></span>

### <span data-ttu-id="38fd4-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="38fd4-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="38fd4-151">System. String</span><span class="sxs-lookup"><span data-stu-id="38fd4-151">System.String</span></span>

### <span data-ttu-id="38fd4-152">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="38fd4-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="38fd4-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="38fd4-153">System.String[]</span></span>

## <span data-ttu-id="38fd4-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38fd4-154">OUTPUTS</span></span>

### <span data-ttu-id="38fd4-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="38fd4-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="38fd4-156">Note</span><span class="sxs-lookup"><span data-stu-id="38fd4-156">NOTES</span></span>

## <span data-ttu-id="38fd4-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38fd4-157">RELATED LINKS</span></span>