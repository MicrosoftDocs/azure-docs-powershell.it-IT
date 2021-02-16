---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208843"
---
# <span data-ttu-id="18cf9-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="18cf9-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="18cf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="18cf9-103">Rimuove un binding SSL da un certificato caricato.</span><span class="sxs-lookup"><span data-stu-id="18cf9-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="18cf9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18cf9-104">SYNTAX</span></span>

### <span data-ttu-id="18cf9-105">S1</span><span class="sxs-lookup"><span data-stu-id="18cf9-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18cf9-106">S2</span><span class="sxs-lookup"><span data-stu-id="18cf9-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18cf9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="18cf9-107">DESCRIPTION</span></span>
<span data-ttu-id="18cf9-108">Il cmdlet **Remove-AzWebAppSSLBinding** rimuove un binding SSL (Secure Sockets Layer) da un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="18cf9-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="18cf9-109">Le associazioni SSL vengono usate per associare un'app Web a un certificato.</span><span class="sxs-lookup"><span data-stu-id="18cf9-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="18cf9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18cf9-110">EXAMPLES</span></span>

### <span data-ttu-id="18cf9-111">Esempio 1: Rimuovere un binding SSL per un'app Web</span><span class="sxs-lookup"><span data-stu-id="18cf9-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="18cf9-112">Questo comando rimuove il binding SSL per l'app Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="18cf9-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="18cf9-113">Poiché il *parametro DeleteCertificate* non è incluso, il certificato verrà eliminato se non ha più binding SSL.</span><span class="sxs-lookup"><span data-stu-id="18cf9-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="18cf9-114">Esempio 2: Rimuovere un binding SSL senza rimuovere il certificato</span><span class="sxs-lookup"><span data-stu-id="18cf9-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="18cf9-115">Come nell'esempio 1, questo comando rimuove anche il binding SSL per l'app Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="18cf9-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="18cf9-116">In questo caso, tuttavia, è incluso *il parametro DeleteCertificate* e il relativo valore è impostato su $False.</span><span class="sxs-lookup"><span data-stu-id="18cf9-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="18cf9-117">Questo significa che il certificato non verrà eliminato indipendentemente dal fatto che abbia o meno binding SSL.</span><span class="sxs-lookup"><span data-stu-id="18cf9-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="18cf9-118">Esempio 3: Usare un riferimento a un oggetto per rimuovere un binding SSL</span><span class="sxs-lookup"><span data-stu-id="18cf9-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="18cf9-119">In questo esempio viene utilizzato un riferimento a un oggetto per il sito Web dell'app Web per rimuovere il binding SSL per un'app Web.</span><span class="sxs-lookup"><span data-stu-id="18cf9-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="18cf9-120">Il primo comando usa il cmdlet Get-AzWebApp per creare un riferimento a un oggetto all'app Web denominato ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="18cf9-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="18cf9-121">Il riferimento all'oggetto viene archiviato in una variabile denominata $WebApp.</span><span class="sxs-lookup"><span data-stu-id="18cf9-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="18cf9-122">Il secondo comando usa il riferimento all'oggetto e il cmdlet **Remove-AzWebAppSSLBinding** per rimuovere il binding SSL.</span><span class="sxs-lookup"><span data-stu-id="18cf9-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="18cf9-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18cf9-123">PARAMETERS</span></span>

### <span data-ttu-id="18cf9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cf9-124">-DefaultProfile</span></span>
<span data-ttu-id="18cf9-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18cf9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18cf9-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="18cf9-126">-DeleteCertificate</span></span>
<span data-ttu-id="18cf9-127">Specifica l'azione da eseguire se il binding SSL da rimuovere è l'unico binding usato dal certificato.</span><span class="sxs-lookup"><span data-stu-id="18cf9-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="18cf9-128">Se *DeleteCertificate* è impostato su $False, il certificato non verrà eliminato quando viene eliminato il binding.</span><span class="sxs-lookup"><span data-stu-id="18cf9-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="18cf9-129">Se *DeleteCertificate* è impostato su $True o non è incluso nel comando, il certificato verrà eliminato insieme al binding SSL.</span><span class="sxs-lookup"><span data-stu-id="18cf9-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="18cf9-130">Il certificato verrà eliminato solo se il binding SSL da rimuovere è l'unico binding usato dal certificato.</span><span class="sxs-lookup"><span data-stu-id="18cf9-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="18cf9-131">Se il certificato ha più di una associazione, il certificato non verrà rimosso indipendentemente dal valore del *parametro DeleteCertificate.*</span><span class="sxs-lookup"><span data-stu-id="18cf9-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18cf9-132">-Force</span><span class="sxs-lookup"><span data-stu-id="18cf9-132">-Force</span></span>
<span data-ttu-id="18cf9-133">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="18cf9-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18cf9-134">-Name</span><span class="sxs-lookup"><span data-stu-id="18cf9-134">-Name</span></span>
<span data-ttu-id="18cf9-135">Specifica il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="18cf9-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="18cf9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18cf9-136">-ResourceGroupName</span></span>
<span data-ttu-id="18cf9-137">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="18cf9-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="18cf9-138">Non è possibile usare *il parametro ResourceGroupName* e il *parametro WebApp* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="18cf9-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18cf9-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="18cf9-139">-Slot</span></span>
<span data-ttu-id="18cf9-140">Specifica lo slot di distribuzione di Web App.</span><span class="sxs-lookup"><span data-stu-id="18cf9-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="18cf9-141">Per ottenere uno slot di distribuzione, usare il cmdlet Get-AzWebAppSlot distribuzione.</span><span class="sxs-lookup"><span data-stu-id="18cf9-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18cf9-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="18cf9-142">-WebApp</span></span>
<span data-ttu-id="18cf9-143">Specifica un'app Web.</span><span class="sxs-lookup"><span data-stu-id="18cf9-143">Specifies a Web App.</span></span>
<span data-ttu-id="18cf9-144">Per ottenere un'app Web, usare il cmdlet Get-AzWebApp web app.</span><span class="sxs-lookup"><span data-stu-id="18cf9-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="18cf9-145">Non è possibile usare *il parametro WebApp* nello stesso comando del *parametro ResourceGroupName* e/o *WebAppName.*</span><span class="sxs-lookup"><span data-stu-id="18cf9-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18cf9-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="18cf9-146">-WebAppName</span></span>
<span data-ttu-id="18cf9-147">Specifica il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="18cf9-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="18cf9-148">Non è possibile usare *il parametro WebAppName* e il *parametro WebApp* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="18cf9-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18cf9-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18cf9-149">-Confirm</span></span>
<span data-ttu-id="18cf9-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18cf9-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18cf9-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18cf9-151">-WhatIf</span></span>
<span data-ttu-id="18cf9-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18cf9-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18cf9-153">Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18cf9-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18cf9-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18cf9-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18cf9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cf9-155">CommonParameters</span></span>
<span data-ttu-id="18cf9-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18cf9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cf9-157">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18cf9-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cf9-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="18cf9-158">INPUTS</span></span>

### <span data-ttu-id="18cf9-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="18cf9-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="18cf9-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18cf9-160">OUTPUTS</span></span>

### <span data-ttu-id="18cf9-161">System.Void</span><span class="sxs-lookup"><span data-stu-id="18cf9-161">System.Void</span></span>

## <span data-ttu-id="18cf9-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="18cf9-162">NOTES</span></span>

## <span data-ttu-id="18cf9-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18cf9-163">RELATED LINKS</span></span>

[<span data-ttu-id="18cf9-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="18cf9-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="18cf9-165">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="18cf9-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="18cf9-166">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18cf9-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="18cf9-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="18cf9-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


