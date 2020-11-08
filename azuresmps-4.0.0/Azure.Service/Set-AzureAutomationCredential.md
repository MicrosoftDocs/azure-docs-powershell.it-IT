---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C92B4B70-4342-4219-80D3-FB79BDC171A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 16fbdf1a0a63fb5a75aa7bc200036a7332ea15f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023789"
---
# <span data-ttu-id="8e562-101">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8e562-101">Set-AzureAutomationCredential</span></span>

## <span data-ttu-id="8e562-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e562-102">SYNOPSIS</span></span>

<span data-ttu-id="8e562-103">Modifica una credenziale nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="8e562-103">Modifies a credential in Automation.</span></span>

## <span data-ttu-id="8e562-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e562-104">SYNTAX</span></span>

```
Set-AzureAutomationCredential -Name <String> [-Description <String>] [-Value <PSCredential>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8e562-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e562-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="8e562-106">Il cmdlet **set-AzureAutomationCredential** modifica una credenziale come oggetto **PSCredential** in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8e562-106">The **Set-AzureAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="8e562-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e562-107">EXAMPLES</span></span>

### <span data-ttu-id="8e562-108">Esempio 1: aggiornare una credenziale</span><span class="sxs-lookup"><span data-stu-id="8e562-108">Example 1: Update a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contos17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="8e562-109">Questi comandi aggiornano una credenziale esistente denominata Credential.</span><span class="sxs-lookup"><span data-stu-id="8e562-109">These commands update an existing credential named MyCredential.</span></span>
<span data-ttu-id="8e562-110">Viene prima creato un oggetto Credential che include un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="8e562-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="8e562-111">Questo viene quindi usato nell'ultimo comando per aggiornare le credenziali di automazione.</span><span class="sxs-lookup"><span data-stu-id="8e562-111">This is then used in the last command to update the automation credential.</span></span>

## <span data-ttu-id="8e562-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e562-112">PARAMETERS</span></span>

### <span data-ttu-id="8e562-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8e562-113">-AutomationAccountName</span></span>
<span data-ttu-id="8e562-114">Specifica il nome dell'account di automazione con le credenziali.</span><span class="sxs-lookup"><span data-stu-id="8e562-114">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="8e562-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e562-115">-Description</span></span>
<span data-ttu-id="8e562-116">Specifica una descrizione per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="8e562-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="8e562-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e562-117">-Name</span></span>
<span data-ttu-id="8e562-118">Specifica il nome della credenziale.</span><span class="sxs-lookup"><span data-stu-id="8e562-118">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="8e562-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="8e562-119">-Profile</span></span>
<span data-ttu-id="8e562-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e562-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8e562-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8e562-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8e562-122">-Valore</span><span class="sxs-lookup"><span data-stu-id="8e562-122">-Value</span></span>
<span data-ttu-id="8e562-123">Specifica le credenziali come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="8e562-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e562-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e562-124">CommonParameters</span></span>
<span data-ttu-id="8e562-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e562-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e562-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e562-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e562-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e562-127">INPUTS</span></span>

## <span data-ttu-id="8e562-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e562-128">OUTPUTS</span></span>

### <span data-ttu-id="8e562-129">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="8e562-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="8e562-130">Note</span><span class="sxs-lookup"><span data-stu-id="8e562-130">NOTES</span></span>

## <span data-ttu-id="8e562-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e562-131">RELATED LINKS</span></span>

[<span data-ttu-id="8e562-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8e562-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="8e562-133">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8e562-133">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="8e562-134">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8e562-134">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)


