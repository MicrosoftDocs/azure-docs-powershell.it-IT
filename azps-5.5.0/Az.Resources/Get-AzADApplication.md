---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 68344fcafa16187651615c95ec2fb41d0bbbfb82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178910"
---
# <span data-ttu-id="bcdda-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bcdda-101">Get-AzADApplication</span></span>

## <span data-ttu-id="bcdda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcdda-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdda-103">Elenca le applicazioni azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="bcdda-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="bcdda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcdda-104">SYNTAX</span></span>

### <span data-ttu-id="bcdda-105">EmptyParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bcdda-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bcdda-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcdda-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bcdda-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcdda-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bcdda-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcdda-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bcdda-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcdda-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bcdda-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcdda-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="bcdda-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bcdda-111">DESCRIPTION</span></span>
<span data-ttu-id="bcdda-112">Elenca le applicazioni azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="bcdda-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="bcdda-113">La ricerca dell'applicazione può essere eseguita da ObjectId, ApplicationId, IdentifierUri o DisplayName.</span><span class="sxs-lookup"><span data-stu-id="bcdda-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="bcdda-114">Se non viene fornito alcun parametro, recupera tutte le applicazioni nel tenant.</span><span class="sxs-lookup"><span data-stu-id="bcdda-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="bcdda-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcdda-115">EXAMPLES</span></span>

### <span data-ttu-id="bcdda-116">Esempio 1 - Elencare tutte le applicazioni</span><span class="sxs-lookup"><span data-stu-id="bcdda-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="bcdda-117">Elenca tutte le applicazioni in un tenant.</span><span class="sxs-lookup"><span data-stu-id="bcdda-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="bcdda-118">Esempio 2 - Applicazioni elenco che usano la suddivisione in pagine</span><span class="sxs-lookup"><span data-stu-id="bcdda-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="bcdda-119">Elenca le prime 100 applicazioni in un tenant.</span><span class="sxs-lookup"><span data-stu-id="bcdda-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="bcdda-120">Esempio 3 - Ottenere l'URI dell'applicazione in base all'identificatore</span><span class="sxs-lookup"><span data-stu-id="bcdda-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="bcdda-121">Ottiene l'applicazione con l'URI identificatore come " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="bcdda-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="bcdda-122">Esempio 4 - Ottenere l'applicazione per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="bcdda-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="bcdda-123">Ottiene l'applicazione con l'ID oggetto '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span><span class="sxs-lookup"><span data-stu-id="bcdda-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="bcdda-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcdda-124">PARAMETERS</span></span>

### <span data-ttu-id="bcdda-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bcdda-125">-ApplicationId</span></span>
<span data-ttu-id="bcdda-126">ID applicazione dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="bcdda-126">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcdda-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdda-127">-DefaultProfile</span></span>
<span data-ttu-id="bcdda-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="bcdda-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcdda-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bcdda-129">-DisplayName</span></span>
<span data-ttu-id="bcdda-130">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bcdda-130">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcdda-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="bcdda-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="bcdda-132">Recuperare tutte le applicazioni a partire dal nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="bcdda-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcdda-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="bcdda-133">-IdentifierUri</span></span>
<span data-ttu-id="bcdda-134">Uri identificatore univoco dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="bcdda-134">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcdda-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bcdda-135">-ObjectId</span></span>
<span data-ttu-id="bcdda-136">ID oggetto dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="bcdda-136">The object id of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcdda-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="bcdda-137">-IncludeTotalCount</span></span>
<span data-ttu-id="bcdda-138">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="bcdda-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="bcdda-139">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="bcdda-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="bcdda-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="bcdda-140">-Skip</span></span>
<span data-ttu-id="bcdda-141">Ignora i primi N oggetti e quindi ottiene gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="bcdda-141">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdda-142">-First</span><span class="sxs-lookup"><span data-stu-id="bcdda-142">-First</span></span>
<span data-ttu-id="bcdda-143">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="bcdda-143">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdda-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdda-144">CommonParameters</span></span>
<span data-ttu-id="bcdda-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcdda-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdda-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bcdda-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdda-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="bcdda-147">INPUTS</span></span>

### <span data-ttu-id="bcdda-148">System.String</span><span class="sxs-lookup"><span data-stu-id="bcdda-148">System.String</span></span>

### <span data-ttu-id="bcdda-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="bcdda-149">System.Guid</span></span>

## <span data-ttu-id="bcdda-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcdda-150">OUTPUTS</span></span>

### <span data-ttu-id="bcdda-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="bcdda-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="bcdda-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="bcdda-152">NOTES</span></span>

## <span data-ttu-id="bcdda-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcdda-153">RELATED LINKS</span></span>

[<span data-ttu-id="bcdda-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bcdda-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="bcdda-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bcdda-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="bcdda-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bcdda-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="bcdda-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bcdda-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="bcdda-158">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bcdda-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="bcdda-159">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bcdda-159">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

