---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: BCF8DAB4-3E14-463B-A18F-E91C740B0D3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 08dd82489bf02efa167386300b9b1d565e1a63de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029955"
---
# <span data-ttu-id="87279-101">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="87279-101">Remove-AzureAutomationCertificate</span></span>

## <span data-ttu-id="87279-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87279-102">SYNOPSIS</span></span>

<span data-ttu-id="87279-103">Rimuove un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="87279-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="87279-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87279-104">SYNTAX</span></span>

```
Remove-AzureAutomationCertificate -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="87279-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87279-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="87279-106">Il cmdlet **Remove-AzureAutomationAccount** rimuove un certificato da Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="87279-106">The **Remove-AzureAutomationAccount** cmdlet removes a certificate from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="87279-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87279-107">EXAMPLES</span></span>

### <span data-ttu-id="87279-108">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="87279-108">Example 1: Remove a certificate</span></span>
```
PS C:\> Remove-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01"
```

<span data-ttu-id="87279-109">Questo comando rimuove un certificato denominato Cert01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="87279-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="87279-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87279-110">PARAMETERS</span></span>

### <span data-ttu-id="87279-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="87279-111">-AutomationAccountName</span></span>
<span data-ttu-id="87279-112">Specifica il nome dell'account di automazione con il certificato.</span><span class="sxs-lookup"><span data-stu-id="87279-112">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="87279-113">-Force</span><span class="sxs-lookup"><span data-stu-id="87279-113">-Force</span></span>
<span data-ttu-id="87279-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="87279-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87279-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="87279-115">-Name</span></span>
<span data-ttu-id="87279-116">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="87279-116">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="87279-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="87279-117">-Profile</span></span>
<span data-ttu-id="87279-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87279-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87279-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="87279-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87279-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87279-120">CommonParameters</span></span>
<span data-ttu-id="87279-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87279-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87279-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87279-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87279-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87279-123">INPUTS</span></span>

## <span data-ttu-id="87279-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87279-124">OUTPUTS</span></span>

## <span data-ttu-id="87279-125">Note</span><span class="sxs-lookup"><span data-stu-id="87279-125">NOTES</span></span>

## <span data-ttu-id="87279-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87279-126">RELATED LINKS</span></span>

[<span data-ttu-id="87279-127">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="87279-127">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="87279-128">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="87279-128">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="87279-129">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="87279-129">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


