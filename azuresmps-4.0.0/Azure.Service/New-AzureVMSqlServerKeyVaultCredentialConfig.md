---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EC6F7790-5E31-4C22-B006-38B5C1868671
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0272740ced33d19e2610a6116812df4a815ea3c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029650"
---
# <span data-ttu-id="9ad46-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="9ad46-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="9ad46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ad46-102">SYNOPSIS</span></span>

## <span data-ttu-id="9ad46-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ad46-103">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ad46-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ad46-104">DESCRIPTION</span></span>

## <span data-ttu-id="9ad46-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ad46-105">EXAMPLES</span></span>

### <span data-ttu-id="9ad46-106">1:</span><span class="sxs-lookup"><span data-stu-id="9ad46-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="9ad46-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ad46-107">PARAMETERS</span></span>

### <span data-ttu-id="9ad46-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="9ad46-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad46-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="9ad46-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad46-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="9ad46-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad46-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9ad46-111">-InformationAction</span></span>
<span data-ttu-id="9ad46-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="9ad46-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9ad46-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9ad46-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9ad46-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="9ad46-114">Continue</span></span>
- <span data-ttu-id="9ad46-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="9ad46-115">Ignore</span></span>
- <span data-ttu-id="9ad46-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="9ad46-116">Inquire</span></span>
- <span data-ttu-id="9ad46-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9ad46-117">SilentlyContinue</span></span>
- <span data-ttu-id="9ad46-118">Stop</span><span class="sxs-lookup"><span data-stu-id="9ad46-118">Stop</span></span>
- <span data-ttu-id="9ad46-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="9ad46-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad46-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9ad46-120">-InformationVariable</span></span>
<span data-ttu-id="9ad46-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="9ad46-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad46-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="9ad46-122">-Profile</span></span>
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

### <span data-ttu-id="9ad46-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9ad46-123">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad46-124">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="9ad46-124">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad46-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad46-125">CommonParameters</span></span>
<span data-ttu-id="9ad46-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad46-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad46-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad46-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad46-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ad46-128">INPUTS</span></span>

## <span data-ttu-id="9ad46-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ad46-129">OUTPUTS</span></span>

## <span data-ttu-id="9ad46-130">Note</span><span class="sxs-lookup"><span data-stu-id="9ad46-130">NOTES</span></span>

## <span data-ttu-id="9ad46-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ad46-131">RELATED LINKS</span></span>

