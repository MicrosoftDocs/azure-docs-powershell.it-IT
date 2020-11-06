---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: d3825b4887d2361a4bb378bfddc3085773efd84b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521111"
---
# <span data-ttu-id="1f7c4-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1f7c4-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="1f7c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7c4-103">Imposta i dettagli dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f7c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f7c4-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f7c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f7c4-105">DESCRIPTION</span></span>
<span data-ttu-id="1f7c4-106">Il cmdlet **set-AzureRmApiManagementUser** imposta i dettagli utente.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="1f7c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f7c4-107">EXAMPLES</span></span>

### <span data-ttu-id="1f7c4-108">Esempio 1: modificare la password di un utente, l'indirizzo di posta elettronica e lo stato</span><span class="sxs-lookup"><span data-stu-id="1f7c4-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="1f7c4-109">Questo comando imposta una nuova password utente e un indirizzo di posta elettronica e blocca l'utente.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="1f7c4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f7c4-110">PARAMETERS</span></span>

### <span data-ttu-id="1f7c4-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1f7c4-111">-Context</span></span>
<span data-ttu-id="1f7c4-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1f7c4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="1f7c4-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-113">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7c4-114">-DefaultProfile</span></span>
<span data-ttu-id="1f7c4-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1f7c4-116">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="1f7c4-116">-Email</span></span>
<span data-ttu-id="1f7c4-117">Specifica l'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="1f7c4-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="1f7c4-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="1f7c4-119">-FirstName</span></span>
<span data-ttu-id="1f7c4-120">Specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="1f7c4-121">Questo parametro deve essere lungo da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="1f7c4-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="1f7c4-122">-LastName</span></span>
<span data-ttu-id="1f7c4-123">Specifica il cognome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="1f7c4-124">Questo parametro deve essere di lunghezza da 1 a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="1f7c4-125">-Nota</span><span class="sxs-lookup"><span data-stu-id="1f7c4-125">-Note</span></span>
<span data-ttu-id="1f7c4-126">Specifica una nota relativa all'utente.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-126">Specifies a note about the user.</span></span>
<span data-ttu-id="1f7c4-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-127">This parameter is optional.</span></span>
<span data-ttu-id="1f7c4-128">Il valore predefinito di questo parametro è $null.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="1f7c4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f7c4-129">-PassThru</span></span>
<span data-ttu-id="1f7c4-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="1f7c4-130">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7c4-131">-Password</span><span class="sxs-lookup"><span data-stu-id="1f7c4-131">-Password</span></span>
<span data-ttu-id="1f7c4-132">Specifica la password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-132">Specifies the user password.</span></span>
<span data-ttu-id="1f7c4-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-133">This parameter is optional.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7c4-134">-Stato</span><span class="sxs-lookup"><span data-stu-id="1f7c4-134">-State</span></span>
<span data-ttu-id="1f7c4-135">Specifica lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-135">Specifies the user state.</span></span>
<span data-ttu-id="1f7c4-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-136">This parameter is optional.</span></span>
<span data-ttu-id="1f7c4-137">Il valore predefinito è attivo.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-137">The default value is Active.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7c4-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="1f7c4-138">-UserId</span></span>
<span data-ttu-id="1f7c4-139">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-139">Specifies the user ID.</span></span>
<span data-ttu-id="1f7c4-140">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-140">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7c4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7c4-141">CommonParameters</span></span>
<span data-ttu-id="1f7c4-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7c4-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f7c4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7c4-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f7c4-144">INPUTS</span></span>

### <span data-ttu-id="1f7c4-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1f7c4-145">None</span></span>
<span data-ttu-id="1f7c4-146">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1f7c4-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f7c4-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f7c4-147">OUTPUTS</span></span>

### <span data-ttu-id="1f7c4-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1f7c4-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="1f7c4-149">Note</span><span class="sxs-lookup"><span data-stu-id="1f7c4-149">NOTES</span></span>

## <span data-ttu-id="1f7c4-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f7c4-150">RELATED LINKS</span></span>

[<span data-ttu-id="1f7c4-151">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1f7c4-151">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="1f7c4-152">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1f7c4-152">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="1f7c4-153">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1f7c4-153">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


