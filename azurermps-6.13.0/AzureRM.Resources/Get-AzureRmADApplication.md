---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: d36bca60f722498beaa831c2a630b23d8a709019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514879"
---
# <span data-ttu-id="f2a89-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f2a89-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="f2a89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2a89-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a89-103">Elenca le applicazioni di Azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="f2a89-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2a89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2a89-104">SYNTAX</span></span>

### <span data-ttu-id="f2a89-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2a89-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f2a89-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2a89-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f2a89-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2a89-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f2a89-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2a89-108">SearchStringParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f2a89-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2a89-109">DisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f2a89-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2a89-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="f2a89-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2a89-111">DESCRIPTION</span></span>
<span data-ttu-id="f2a89-112">Elenca le applicazioni di Azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="f2a89-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="f2a89-113">La ricerca dell'applicazione può essere eseguita da ObjectId, ApplicationId, IdentifierUri o DisplayName.</span><span class="sxs-lookup"><span data-stu-id="f2a89-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="f2a89-114">Se non viene specificato alcun parametro, recupera tutte le applicazioni sotto il tenant.</span><span class="sxs-lookup"><span data-stu-id="f2a89-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="f2a89-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2a89-115">EXAMPLES</span></span>

### <span data-ttu-id="f2a89-116">Esempio 1-elenca tutte le applicazioni</span><span class="sxs-lookup"><span data-stu-id="f2a89-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzureRmADApplication
```

<span data-ttu-id="f2a89-117">Elenca tutte le applicazioni in un tenant.</span><span class="sxs-lookup"><span data-stu-id="f2a89-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="f2a89-118">Esempio 2-elenco delle applicazioni che usano il paging</span><span class="sxs-lookup"><span data-stu-id="f2a89-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzureRmADApplication -First 100
```

<span data-ttu-id="f2a89-119">Elenca le prime applicazioni di 100 in un tenant.</span><span class="sxs-lookup"><span data-stu-id="f2a89-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="f2a89-120">Esempio 3-ottenere l'applicazione dall'URI dell'identificatore</span><span class="sxs-lookup"><span data-stu-id="f2a89-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="f2a89-121">Ottiene l'applicazione con URI dell'identificatore come " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="f2a89-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="f2a89-122">Esempio 4-ottenere l'applicazione dall'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="f2a89-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="f2a89-123">Ottiene l'applicazione con l'ID oggetto "39e64ec6-569B-4030-8e1c-c3c519a05d69".</span><span class="sxs-lookup"><span data-stu-id="f2a89-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="f2a89-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2a89-124">PARAMETERS</span></span>

### <span data-ttu-id="f2a89-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f2a89-125">-ApplicationId</span></span>
<span data-ttu-id="f2a89-126">ID applicazione dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f2a89-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="f2a89-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a89-127">-DefaultProfile</span></span>
<span data-ttu-id="f2a89-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f2a89-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2a89-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f2a89-129">-DisplayName</span></span>
<span data-ttu-id="f2a89-130">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2a89-130">The display name of the application.</span></span>

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

### <span data-ttu-id="f2a89-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="f2a89-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="f2a89-132">Recuperare tutte le applicazioni che iniziano con il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f2a89-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="f2a89-133">-Primo</span><span class="sxs-lookup"><span data-stu-id="f2a89-133">-First</span></span>
<span data-ttu-id="f2a89-134">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="f2a89-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="f2a89-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="f2a89-135">-IdentifierUri</span></span>
<span data-ttu-id="f2a89-136">URI identificatore univoco dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f2a89-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="f2a89-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="f2a89-137">-IncludeTotalCount</span></span>
<span data-ttu-id="f2a89-138">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="f2a89-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="f2a89-139">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="f2a89-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="f2a89-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f2a89-140">-ObjectId</span></span>
<span data-ttu-id="f2a89-141">ID oggetto dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f2a89-141">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a89-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="f2a89-142">-Skip</span></span>
<span data-ttu-id="f2a89-143">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="f2a89-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="f2a89-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a89-144">CommonParameters</span></span>
<span data-ttu-id="f2a89-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2a89-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a89-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2a89-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a89-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2a89-147">INPUTS</span></span>

### <span data-ttu-id="f2a89-148">System. Guid</span><span class="sxs-lookup"><span data-stu-id="f2a89-148">System.Guid</span></span>

### <span data-ttu-id="f2a89-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f2a89-149">System.String</span></span>

## <span data-ttu-id="f2a89-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2a89-150">OUTPUTS</span></span>

### <span data-ttu-id="f2a89-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="f2a89-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="f2a89-152">Note</span><span class="sxs-lookup"><span data-stu-id="f2a89-152">NOTES</span></span>

## <span data-ttu-id="f2a89-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2a89-153">RELATED LINKS</span></span>

[<span data-ttu-id="f2a89-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f2a89-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="f2a89-155">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f2a89-155">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="f2a89-156">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f2a89-156">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="f2a89-157">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f2a89-157">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="f2a89-158">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f2a89-158">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="f2a89-159">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f2a89-159">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

