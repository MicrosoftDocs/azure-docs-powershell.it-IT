---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 52e5dce154b6798a0bddb0416235d371d6c85910
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516332"
---
# <span data-ttu-id="7d6ef-101">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7d6ef-101">Remove-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="7d6ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d6ef-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6ef-103">Rimuove un binding SSL da un certificato caricato.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-103">Removes an SSL binding from an uploaded certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d6ef-104">SYNTAX</span></span>

### <span data-ttu-id="7d6ef-105">S1</span><span class="sxs-lookup"><span data-stu-id="7d6ef-105">S1</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6ef-106">S2</span><span class="sxs-lookup"><span data-stu-id="7d6ef-106">S2</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d6ef-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d6ef-107">DESCRIPTION</span></span>
<span data-ttu-id="7d6ef-108">Il cmdlet **Remove-AzureRmWebAppSSLBinding** rimuove un binding SSL (Secure Sockets Layer) da un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-108">The **Remove-AzureRmWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="7d6ef-109">I binding SSL vengono usati per associare un'app Web a un certificato.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="7d6ef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d6ef-110">EXAMPLES</span></span>

### <span data-ttu-id="7d6ef-111">Esempio 1: rimuovere un binding SSL per un'app Web</span><span class="sxs-lookup"><span data-stu-id="7d6ef-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="7d6ef-112">Questo comando rimuove il binding SSL per l'app Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="7d6ef-113">Dato che il parametro *DeleteCertificate* non è incluso, il certificato verrà eliminato se non ha più binding SSL.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="7d6ef-114">Esempio 2: rimuovere un binding SSL senza rimuovere il certificato</span><span class="sxs-lookup"><span data-stu-id="7d6ef-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="7d6ef-115">Analogamente all'esempio 1, questo comando rimuove anche il binding SSL per l'app Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="7d6ef-116">In questo caso, tuttavia, il parametro *DeleteCertificate* è incluso e il valore del parametro è impostato su $false.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="7d6ef-117">Ciò significa che il certificato non verrà eliminato indipendentemente dal fatto che disponga di binding SSL o meno.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="7d6ef-118">Esempio 3: usare un riferimento a un oggetto per rimuovere un binding SSL</span><span class="sxs-lookup"><span data-stu-id="7d6ef-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="7d6ef-119">In questo esempio viene usato un riferimento a un oggetto al sito Web dell'app per rimuovere il binding SSL per un'app Web.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="7d6ef-120">Il primo comando usa il cmdlet Get-AzureRmWebApp per creare un riferimento a un oggetto all'app Web denominata ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-120">The first command uses the Get-AzureRmWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="7d6ef-121">Il riferimento a un oggetto viene archiviato in una variabile denominata $WebApp.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="7d6ef-122">Il secondo comando usa il riferimento oggetto e il cmdlet **Remove-AzureRmWebAppSSLBinding** per rimuovere il binding SSL.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-122">The second command uses the object reference and the **Remove-AzureRmWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="7d6ef-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d6ef-123">PARAMETERS</span></span>

### <span data-ttu-id="7d6ef-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6ef-124">-DefaultProfile</span></span>
<span data-ttu-id="7d6ef-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d6ef-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="7d6ef-126">-DeleteCertificate</span></span>
<span data-ttu-id="7d6ef-127">Specifica l'azione da eseguire se il binding SSL da rimuovere è l'unico binding usato dal certificato.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="7d6ef-128">Se *DeleteCertificate* è impostato su $false, il certificato non verrà eliminato quando l'associazione viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="7d6ef-129">Se *DeleteCertificate* è impostato su $true o non è incluso nel comando, il certificato verrà eliminato insieme al binding SSL.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="7d6ef-130">Il certificato verrà eliminato solo se il binding SSL da rimuovere è l'unico binding usato dal certificato.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="7d6ef-131">Se il certificato contiene più di un binding, il certificato non verrà rimosso indipendentemente dal valore del parametro *DeleteCertificate* .</span><span class="sxs-lookup"><span data-stu-id="7d6ef-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

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

### <span data-ttu-id="7d6ef-132">-Force</span><span class="sxs-lookup"><span data-stu-id="7d6ef-132">-Force</span></span>
<span data-ttu-id="7d6ef-133">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d6ef-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d6ef-134">-Name</span></span>
<span data-ttu-id="7d6ef-135">Specifica il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="7d6ef-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6ef-136">-ResourceGroupName</span></span>
<span data-ttu-id="7d6ef-137">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="7d6ef-138">Non è possibile usare il parametro *ResourceGroupName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="7d6ef-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="7d6ef-139">-Slot</span></span>
<span data-ttu-id="7d6ef-140">Specifica lo slot di distribuzione dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="7d6ef-141">Per ottenere uno slot di distribuzione, usare il cmdlet Get-AzureRMWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-141">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="7d6ef-142">-Web App</span><span class="sxs-lookup"><span data-stu-id="7d6ef-142">-WebApp</span></span>
<span data-ttu-id="7d6ef-143">Specifica un'app Web.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-143">Specifies a Web App.</span></span>
<span data-ttu-id="7d6ef-144">Per ottenere un'app Web, usa il cmdlet Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-144">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>
<span data-ttu-id="7d6ef-145">Non è possibile usare il parametro *Web App* nello stesso comando del parametro *ResourceGroupName* e/o *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="7d6ef-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="7d6ef-146">-WebAppName</span></span>
<span data-ttu-id="7d6ef-147">Specifica il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="7d6ef-148">Non è possibile usare il parametro *WebAppName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="7d6ef-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d6ef-149">-Confirm</span></span>
<span data-ttu-id="7d6ef-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d6ef-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6ef-151">-WhatIf</span></span>
<span data-ttu-id="7d6ef-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6ef-153">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6ef-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d6ef-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6ef-155">CommonParameters</span></span>
<span data-ttu-id="7d6ef-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6ef-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6ef-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6ef-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6ef-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d6ef-158">INPUTS</span></span>

### <span data-ttu-id="7d6ef-159">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="7d6ef-159">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="7d6ef-160">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7d6ef-160">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="7d6ef-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d6ef-161">OUTPUTS</span></span>

### <span data-ttu-id="7d6ef-162">System. void</span><span class="sxs-lookup"><span data-stu-id="7d6ef-162">System.Void</span></span>

## <span data-ttu-id="7d6ef-163">Note</span><span class="sxs-lookup"><span data-stu-id="7d6ef-163">NOTES</span></span>

## <span data-ttu-id="7d6ef-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d6ef-164">RELATED LINKS</span></span>

[<span data-ttu-id="7d6ef-165">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7d6ef-165">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="7d6ef-166">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7d6ef-166">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="7d6ef-167">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7d6ef-167">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="7d6ef-168">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d6ef-168">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


