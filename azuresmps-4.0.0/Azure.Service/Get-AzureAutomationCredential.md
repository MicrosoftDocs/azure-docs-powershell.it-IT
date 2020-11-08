---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023617"
---
# <span data-ttu-id="e9b59-101">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e9b59-101">Get-AzureAutomationCredential</span></span>

## <span data-ttu-id="e9b59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9b59-102">SYNOPSIS</span></span>

<span data-ttu-id="e9b59-103">Ottiene una credenziale di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b59-103">Gets an Azure Automation credential.</span></span>

## <span data-ttu-id="e9b59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9b59-104">SYNTAX</span></span>

### <span data-ttu-id="e9b59-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e9b59-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e9b59-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e9b59-106">ByName</span></span>
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9b59-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9b59-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e9b59-108">Il cmdlet **Get-AzureAutomationCredential** ottiene una o più credenziali di automazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b59-108">The **Get-AzureAutomationCredential** cmdlet gets one or more Microsoft Azure Automation credentials.</span></span>
<span data-ttu-id="e9b59-109">Per impostazione predefinita, vengono restituite tutte le credenziali.</span><span class="sxs-lookup"><span data-stu-id="e9b59-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="e9b59-110">Per ottenere una specifica credenziale, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="e9b59-110">To get a specific credential, specify its name.</span></span>

## <span data-ttu-id="e9b59-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9b59-111">EXAMPLES</span></span>

### <span data-ttu-id="e9b59-112">Esempio 1: ottenere tutte le credenziali</span><span class="sxs-lookup"><span data-stu-id="e9b59-112">Example 1: Get all credentials</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

<span data-ttu-id="e9b59-113">Questo comando consente di ottenere tutte le credenziali nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e9b59-113">This command gets all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e9b59-114">Esempio 2: ottenere una credenziale</span><span class="sxs-lookup"><span data-stu-id="e9b59-114">Example 2: Get a credential</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="e9b59-115">Questo comando ottiene le credenziali denominate credenziale.</span><span class="sxs-lookup"><span data-stu-id="e9b59-115">This command gets the credential named MyCredential.</span></span>

## <span data-ttu-id="e9b59-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9b59-116">PARAMETERS</span></span>

### <span data-ttu-id="e9b59-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e9b59-117">-AutomationAccountName</span></span>
<span data-ttu-id="e9b59-118">Specifica il nome dell'account di automazione con le credenziali da recuperare.</span><span class="sxs-lookup"><span data-stu-id="e9b59-118">Specifies the name of the automation account with the credential to retrieve.</span></span>

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

### <span data-ttu-id="e9b59-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9b59-119">-Name</span></span>
<span data-ttu-id="e9b59-120">Specifica il nome di una credenziale da recuperare.</span><span class="sxs-lookup"><span data-stu-id="e9b59-120">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b59-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="e9b59-121">-Profile</span></span>
<span data-ttu-id="e9b59-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9b59-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9b59-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e9b59-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b59-124">CommonParameters</span></span>
<span data-ttu-id="e9b59-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b59-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b59-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b59-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9b59-127">INPUTS</span></span>

## <span data-ttu-id="e9b59-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9b59-128">OUTPUTS</span></span>

### <span data-ttu-id="e9b59-129">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="e9b59-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="e9b59-130">Note</span><span class="sxs-lookup"><span data-stu-id="e9b59-130">NOTES</span></span>

## <span data-ttu-id="e9b59-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9b59-131">RELATED LINKS</span></span>

[<span data-ttu-id="e9b59-132">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e9b59-132">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="e9b59-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e9b59-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="e9b59-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e9b59-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


