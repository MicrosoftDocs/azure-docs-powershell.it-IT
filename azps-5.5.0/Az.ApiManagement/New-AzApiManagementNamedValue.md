---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190359"
---
# <span data-ttu-id="1237a-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="1237a-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="1237a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1237a-102">SYNOPSIS</span></span>
<span data-ttu-id="1237a-103">Crea un nuovo valore denominato.</span><span class="sxs-lookup"><span data-stu-id="1237a-103">Creates new Named Value.</span></span>

## <span data-ttu-id="1237a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1237a-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1237a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1237a-105">DESCRIPTION</span></span>
<span data-ttu-id="1237a-106">Il cmdlet **New-AzApiManagementNamedValue** crea un valore denominato Gestione API **di** Azure.</span><span class="sxs-lookup"><span data-stu-id="1237a-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="1237a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1237a-107">EXAMPLES</span></span>

### <span data-ttu-id="1237a-108">Esempio 1: Creare un valore denominato che include tag</span><span class="sxs-lookup"><span data-stu-id="1237a-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="1237a-109">Il primo comando assegna due valori alla variabile $Tags variabile.</span><span class="sxs-lookup"><span data-stu-id="1237a-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="1237a-110">Il secondo comando crea un valore denominato e assegna le stringhe in $Tags come tag per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="1237a-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="1237a-111">Esempio 2: Creare un valore denominato con un valore segreto</span><span class="sxs-lookup"><span data-stu-id="1237a-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="1237a-112">Questo comando crea un **valore** denominato con un valore crittografato.</span><span class="sxs-lookup"><span data-stu-id="1237a-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="1237a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1237a-113">PARAMETERS</span></span>

### <span data-ttu-id="1237a-114">-Context</span><span class="sxs-lookup"><span data-stu-id="1237a-114">-Context</span></span>
<span data-ttu-id="1237a-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1237a-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1237a-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1237a-116">This parameter is required.</span></span>

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

### <span data-ttu-id="1237a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1237a-117">-DefaultProfile</span></span>
<span data-ttu-id="1237a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1237a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1237a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1237a-119">-Name</span></span>
<span data-ttu-id="1237a-120">Nome del valore denominato.</span><span class="sxs-lookup"><span data-stu-id="1237a-120">Name of the named value.</span></span>
<span data-ttu-id="1237a-121">La lunghezza massima è 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1237a-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="1237a-122">Può contenere solo lettere, cifre, punto, trattino e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="1237a-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="1237a-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1237a-123">This parameter is required.</span></span>

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

### <span data-ttu-id="1237a-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="1237a-124">-NamedValueId</span></span>
<span data-ttu-id="1237a-125">Identificatore del nuovo valore denominato.</span><span class="sxs-lookup"><span data-stu-id="1237a-125">Identifier of new named value.</span></span>
<span data-ttu-id="1237a-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1237a-126">This parameter is optional.</span></span>
<span data-ttu-id="1237a-127">Se non viene specificato, verrà generato.</span><span class="sxs-lookup"><span data-stu-id="1237a-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="1237a-128">-Secret</span><span class="sxs-lookup"><span data-stu-id="1237a-128">-Secret</span></span>
<span data-ttu-id="1237a-129">Determina se il valore è un segreto e deve essere crittografato o meno.</span><span class="sxs-lookup"><span data-stu-id="1237a-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="1237a-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1237a-130">This parameter is optional.</span></span>
<span data-ttu-id="1237a-131">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="1237a-131">Default Value is false.</span></span>

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

### <span data-ttu-id="1237a-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="1237a-132">-Tag</span></span>
<span data-ttu-id="1237a-133">Tag da associare al valore denominato.</span><span class="sxs-lookup"><span data-stu-id="1237a-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="1237a-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1237a-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="1237a-135">-Value</span><span class="sxs-lookup"><span data-stu-id="1237a-135">-Value</span></span>
<span data-ttu-id="1237a-136">Valore del valore denominato.</span><span class="sxs-lookup"><span data-stu-id="1237a-136">Value of the named value.</span></span>
<span data-ttu-id="1237a-137">Può contenere espressioni per i criteri.</span><span class="sxs-lookup"><span data-stu-id="1237a-137">Can contain policy expressions.</span></span>
<span data-ttu-id="1237a-138">La lunghezza massima è 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1237a-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="1237a-139">Non può essere vuoto o costituito solo da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="1237a-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="1237a-140">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1237a-140">This parameter is required.</span></span>

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

### <span data-ttu-id="1237a-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1237a-141">-Confirm</span></span>
<span data-ttu-id="1237a-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1237a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1237a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1237a-143">-WhatIf</span></span>
<span data-ttu-id="1237a-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1237a-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1237a-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1237a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1237a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1237a-146">CommonParameters</span></span>
<span data-ttu-id="1237a-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1237a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1237a-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1237a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1237a-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="1237a-149">INPUTS</span></span>

### <span data-ttu-id="1237a-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1237a-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1237a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="1237a-151">System.String</span></span>

### <span data-ttu-id="1237a-152">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1237a-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1237a-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1237a-153">System.String[]</span></span>

## <span data-ttu-id="1237a-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1237a-154">OUTPUTS</span></span>

### <span data-ttu-id="1237a-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="1237a-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="1237a-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="1237a-156">NOTES</span></span>

## <span data-ttu-id="1237a-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1237a-157">RELATED LINKS</span></span>
