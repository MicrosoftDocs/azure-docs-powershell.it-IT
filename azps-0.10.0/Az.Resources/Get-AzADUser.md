---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 34a00ed29d40d8824ac0f2d24f5275bb7c0a0164
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862622"
---
# <span data-ttu-id="db1fd-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="db1fd-101">Get-AzADUser</span></span>

## <span data-ttu-id="db1fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="db1fd-103">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db1fd-103">Filters active directory users.</span></span>

## <span data-ttu-id="db1fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db1fd-104">SYNTAX</span></span>

### <span data-ttu-id="db1fd-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db1fd-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db1fd-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1fd-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db1fd-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1fd-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db1fd-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1fd-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db1fd-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1fd-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db1fd-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="db1fd-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="db1fd-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db1fd-111">DESCRIPTION</span></span>
<span data-ttu-id="db1fd-112">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db1fd-112">Filters active directory users.</span></span>

## <span data-ttu-id="db1fd-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db1fd-113">EXAMPLES</span></span>

### <span data-ttu-id="db1fd-114">Esempio 1-elenca tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="db1fd-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="db1fd-115">Elenca tutti gli utenti degli annunci in un tenant.</span><span class="sxs-lookup"><span data-stu-id="db1fd-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="db1fd-116">Esempio 2-elenca tutti gli utenti che usano il paging</span><span class="sxs-lookup"><span data-stu-id="db1fd-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="db1fd-117">Elenca i primi utenti di annunci di 100 in un tenant.</span><span class="sxs-lookup"><span data-stu-id="db1fd-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="db1fd-118">Esempio 3-ottenere l'utente degli annunci per nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="db1fd-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="db1fd-119">Ottiene l'utente dell'annuncio con il nome dell'entità utente " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="db1fd-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="db1fd-120">Esempio 4-elenco per stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="db1fd-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="db1fd-121">Elenca tutti gli utenti di Active Directory il cui nome visualizzato inizia con "Joe".</span><span class="sxs-lookup"><span data-stu-id="db1fd-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="db1fd-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db1fd-122">PARAMETERS</span></span>

### <span data-ttu-id="db1fd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db1fd-123">-DefaultProfile</span></span>
<span data-ttu-id="db1fd-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="db1fd-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db1fd-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db1fd-125">-DisplayName</span></span>
<span data-ttu-id="db1fd-126">Nome visualizzato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="db1fd-126">The display name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db1fd-127">-Primo</span><span class="sxs-lookup"><span data-stu-id="db1fd-127">-First</span></span>
<span data-ttu-id="db1fd-128">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="db1fd-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="db1fd-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="db1fd-129">-IncludeTotalCount</span></span>
<span data-ttu-id="db1fd-130">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="db1fd-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="db1fd-131">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="db1fd-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="db1fd-132">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="db1fd-132">-Mail</span></span>
<span data-ttu-id="db1fd-133">Messaggio di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="db1fd-133">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db1fd-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="db1fd-134">-ObjectId</span></span>
<span data-ttu-id="db1fd-135">ID oggetto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="db1fd-135">Object id of the user.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db1fd-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="db1fd-136">-Skip</span></span>
<span data-ttu-id="db1fd-137">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="db1fd-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="db1fd-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="db1fd-138">-StartsWith</span></span>
<span data-ttu-id="db1fd-139">Usato per trovare gli utenti che iniziano con la stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="db1fd-139">Used to find users that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db1fd-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="db1fd-140">-UserPrincipalName</span></span>
<span data-ttu-id="db1fd-141">UPN dell'utente.</span><span class="sxs-lookup"><span data-stu-id="db1fd-141">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db1fd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db1fd-142">CommonParameters</span></span>
<span data-ttu-id="db1fd-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db1fd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db1fd-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db1fd-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db1fd-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db1fd-145">INPUTS</span></span>

### <span data-ttu-id="db1fd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="db1fd-146">System.String</span></span>

### <span data-ttu-id="db1fd-147">System. Guid</span><span class="sxs-lookup"><span data-stu-id="db1fd-147">System.Guid</span></span>

## <span data-ttu-id="db1fd-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db1fd-148">OUTPUTS</span></span>

### <span data-ttu-id="db1fd-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="db1fd-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="db1fd-150">Note</span><span class="sxs-lookup"><span data-stu-id="db1fd-150">NOTES</span></span>

## <span data-ttu-id="db1fd-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db1fd-151">RELATED LINKS</span></span>

[<span data-ttu-id="db1fd-152">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="db1fd-152">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="db1fd-153">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="db1fd-153">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="db1fd-154">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="db1fd-154">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

