---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 18b5f64426b0a3c458ea489d27781f1a01336b52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677419"
---
# <span data-ttu-id="c5c12-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c5c12-101">Get-AzADApplication</span></span>

## <span data-ttu-id="c5c12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5c12-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c12-103">Elenca le applicazioni di Azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="c5c12-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="c5c12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5c12-104">SYNTAX</span></span>

### <span data-ttu-id="c5c12-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5c12-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c5c12-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c12-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c5c12-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c12-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c5c12-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c12-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c5c12-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c12-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c5c12-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c12-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="c5c12-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5c12-111">DESCRIPTION</span></span>
<span data-ttu-id="c5c12-112">Elenca le applicazioni di Azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="c5c12-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="c5c12-113">La ricerca dell'applicazione può essere eseguita da ObjectId, ApplicationId, IdentifierUri o DisplayName.</span><span class="sxs-lookup"><span data-stu-id="c5c12-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="c5c12-114">Se non viene specificato alcun parametro, recupera tutte le applicazioni sotto il tenant.</span><span class="sxs-lookup"><span data-stu-id="c5c12-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="c5c12-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5c12-115">EXAMPLES</span></span>

### <span data-ttu-id="c5c12-116">Esempio 1-elenca tutte le applicazioni</span><span class="sxs-lookup"><span data-stu-id="c5c12-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="c5c12-117">Elenca tutte le applicazioni in un tenant.</span><span class="sxs-lookup"><span data-stu-id="c5c12-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="c5c12-118">Esempio 2-elenco delle applicazioni che usano il paging</span><span class="sxs-lookup"><span data-stu-id="c5c12-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="c5c12-119">Elenca le prime applicazioni di 100 in un tenant.</span><span class="sxs-lookup"><span data-stu-id="c5c12-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="c5c12-120">Esempio 3-ottenere l'applicazione dall'URI dell'identificatore</span><span class="sxs-lookup"><span data-stu-id="c5c12-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="c5c12-121">Ottiene l'applicazione con URI dell'identificatore come " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="c5c12-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="c5c12-122">Esempio 4-ottenere l'applicazione dall'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="c5c12-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="c5c12-123">Ottiene l'applicazione con l'ID oggetto "39e64ec6-569B-4030-8e1c-c3c519a05d69".</span><span class="sxs-lookup"><span data-stu-id="c5c12-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="c5c12-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5c12-124">PARAMETERS</span></span>

### <span data-ttu-id="c5c12-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c5c12-125">-ApplicationId</span></span>
<span data-ttu-id="c5c12-126">ID applicazione dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="c5c12-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="c5c12-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c12-127">-DefaultProfile</span></span>
<span data-ttu-id="c5c12-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c5c12-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5c12-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c5c12-129">-DisplayName</span></span>
<span data-ttu-id="c5c12-130">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c5c12-130">The display name of the application.</span></span>

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

### <span data-ttu-id="c5c12-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="c5c12-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="c5c12-132">Recuperare tutte le applicazioni che iniziano con il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="c5c12-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="c5c12-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="c5c12-133">-IdentifierUri</span></span>
<span data-ttu-id="c5c12-134">URI identificatore univoco dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="c5c12-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="c5c12-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c5c12-135">-ObjectId</span></span>
<span data-ttu-id="c5c12-136">ID oggetto dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="c5c12-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="c5c12-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="c5c12-137">-IncludeTotalCount</span></span>
<span data-ttu-id="c5c12-138">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="c5c12-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="c5c12-139">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="c5c12-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="c5c12-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="c5c12-140">-Skip</span></span>
<span data-ttu-id="c5c12-141">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="c5c12-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="c5c12-142">-Primo</span><span class="sxs-lookup"><span data-stu-id="c5c12-142">-First</span></span>
<span data-ttu-id="c5c12-143">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="c5c12-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="c5c12-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c12-144">CommonParameters</span></span>
<span data-ttu-id="c5c12-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5c12-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c12-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5c12-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c12-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5c12-147">INPUTS</span></span>

### <span data-ttu-id="c5c12-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c5c12-148">System.String</span></span>

### <span data-ttu-id="c5c12-149">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c5c12-149">System.Guid</span></span>

## <span data-ttu-id="c5c12-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5c12-150">OUTPUTS</span></span>

### <span data-ttu-id="c5c12-151">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c5c12-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c5c12-152">Note</span><span class="sxs-lookup"><span data-stu-id="c5c12-152">NOTES</span></span>

## <span data-ttu-id="c5c12-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5c12-153">RELATED LINKS</span></span>

[<span data-ttu-id="c5c12-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c5c12-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="c5c12-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c5c12-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="c5c12-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c5c12-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="c5c12-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c5c12-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="c5c12-158">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c5c12-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="c5c12-159">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c5c12-159">New-AzADApplication</span></span>](./New-AzADApplication.md)

